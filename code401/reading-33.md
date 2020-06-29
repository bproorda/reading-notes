# React Native And Xamarin

## React Native
   - An open source framework to allow developers to create apps for Android and iOS
   - Snack Player is a useful tool to practice with React Native
   - Just like React, can use both class component and function components with hooks
   - a view is the basic building block of UI: a small rectangular element on the screen which can be used to display text, images, or respond to user input
   - Core Compenents
     - `<View>` Android: `<ViewGroup>` iOS: `<UIView>` Web: `<div>`
     - `<Text>` Android: `<TextView>` iOS: `<UITextView>` Web: `<p>`
     - `<Image>` Android: `<ImageView>` iOS: `<UIImageView>` Web: `<img>`
     - `<ScrollView>` Android: `<ScrollView>` iOS: `<UIScrollView>` Web: `<div>`
     - `<TextInput>` Android: `<EditText>` iOS: `<UITextField>` Web: `<input type text>`

## Xamarin
   - Xamarin is an open-source platform for building modern and performant applications for iOS, Android, and Windows with .NET
   - an abstraction layer that manages communication of shared code with underlying platform code. Xamarin runs in a managed environment that provides conveniences such as memory allocation and garbage collection.
   - allows developers to write all of their business logic in a single language (or reuse existing application code) but achieve native performance, look, and feel on each platform.
   - In a Xamarin.Forms project, we define the UI and event handler code just once and every type is interpreted based on the platform on which the app is running.
     -  iOS UIButton
     - Android.Widget.Button
   - Xamarin.Essentials handles many of the common needs of mobile apps that don't have to do with the UI
     - GPS, the accelerometer, and battery and network states.
   - to create a new one
     - search for mobile, select Mobile App (Xamarin.Forms)
     - choose either template or blank
     - creates there projects, one for android, iOS, and one for code common for both. The first two are called head projects
     - developer can add more head projects for use across more platforms
    - 
