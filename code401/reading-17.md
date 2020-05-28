# Views

- **layout**
    - Razor views have a Layout property
    - `{ @Layout = "_Layout"; }`
    - every layout must call RenderBody
    - Layouts normally in views/shared
    - The layout defines a top level template for views in the app
    - a layout can also use RenderSection to call a section of the layout
    - Views and pages can use Razor directives to import namespaces and use dependency injection
- **Partial Views**
    - A partial view is a Razor markup file (.cshtml) that renders HTML output within another markup file's rendered output.
    - partial views break up bigger markup files and help to avoid code duplication
    - partial view names often start with "_"
    - can use partial tag helper `<partial name="_PartialName" />` or `<partial name="_PartialName.cshtml" />`
    - when using html helper, use PartialAsync, `@await Html.PartialAsync("_PartialName")`
    - When a partial view is instantiated, it receives a copy of the parent's ViewData dictionary.
    - `@await Html.PartialAsync("_PartialName", customViewData)`
- **Tag Helpers**
    - Tag Helpers enable server-side code to participate in creating and rendering HTML elements in Razor files
    - For the most part, Razor markup using Tag Helpers looks like standard HTML.
    - Most built-in Tag Helpers target standard HTML elements and provide server-side attributes for the element.
    - `public class Movie {public string title}` -> `<label asp-for="Movie.title"></label>`
    - the previous lines generate -> `<label for="Movie_title">Title</label>`
    - Tag Helpers scope is controlled by a combination of @addTagHelper, @removeTagHelper, and the "!" opt-out character.
    - @addTagHelper makes tag helpers available
    - You can disable a Tag Helper at the element level with the Tag Helper opt-out character ("!"). 
    