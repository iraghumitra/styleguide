**Practical Guidelines that can be followed for angular + bootstratp based app**

**ANGULAR:**

A lot of guidelines are already proposed by angular team in their docs which when followed creates a good consistent code base. You can check the angular2 style guide here<<https://angular.io/docs/ts/latest/guide/style-guide.html>>. While the guide talks in length about anguar code(Javascript/Typescript)  it doesn't talk about standards for html and css and hence creating the need of this doc.

**HTML & CSS:**

There are many good style guides out there we can follow them as is or cherry pick the items as we like. I personally liked the following.

<https://google.github.io/styleguide/htmlcssguide.xml>

<https://github.com/airbnb/css>

You can look at more style guides at <http://styleguides.io/>

While these style guides talk about general HTML/CSS we can have few more guidelines around angular component templates and styles.

1. We can follow BEM naming conventions for all css files (<https://css-tricks.com/bem-101/>)

2. Keep the style of the component within the component, do not add it to the global styles

3. Prefer overwriting the styles instead of creating a new class.

   Ex: if we have a global style as .btn{min-width:100px} and we want a button to have min-width of 200px in the component style you can overwrite it as .btn{min-width:200px} instead of defining new class like .btn-someother{min-width:200px} this will ensure that we can have a common place to add any new attributes to buttons in the future.

4. Add all the colors and any other variables that are used in theming of the appication to _variables.scss. This will help us to re-theme the application.

5. Use the bootstrap components and layouts as much as possible.
