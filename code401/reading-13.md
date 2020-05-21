# Intro to APIs

**Data Seeding**
  - process of populating a database with an intial set of data
  - can be one with
    - Model seed data
    - Manual migration customization
    - Custom initialization logic
  -  seeding data can be associated with an entity type as part of the model configuration.
  - EF Core migrations can automatically compute what insert, update or delete operations need to be applied when upgrading the database to a new version of the model.
  - example of seeding date:
    - `modelBuilder.Entity<Blog>().HasData(new Blog {BlogId = 1, Url = "http://sample.com"});`
  - To add entities that have a relationship the foreign key values need to be specified:
    - `modelBuilder.Entity<Post>().HasData(
    new Post() { BlogId = 1, PostId = 1, Title = "First post", Content = "Test 1" });`
  - Once the data has been added to the model, migrations should be used to apply the changes
  - `context.Database.EnsureCreated()` can also be used to create a database containing seed data
  - Manual Migration
    - `migrationBuilder.InsertData( table: "Blogs", columns: new[] { "Url" }, values: new object[] { "http://generated.com" });`
  - Custom Initialization Logic
    - A straightforward and powerful way to perform data seeding is to use DbContext.SaveChanges() before the main application logic begins execution.
    - ```
       using (var context = new DataSeedingContext())
        {
         context.Database.EnsureCreated();

        var testBlog = context.Blogs.FirstOrDefault(b => b.Url == "http://test.com");
         if (testBlog == null)
        {
        context.Blogs.Add(new Blog { Url = "http://test.com" });
        }
        context.SaveChanges();
       }
      ```
    