# Practice writing CSS

This code is meant as a learning tool for writing CSS. The `Home` (index.html) page and a regular `Page` (page.html) are provided with default semantic HTML markup.

The __goal__ is to style the provided markup with custom CSS classes so that it matches the screenshots provided in the `/screenshots` directory. There are screenshots for both the `Home` page and the regular `Page`.

## Tips

1. Don't worry about [Responsive Design](https://developers.google.com/web/fundamentals/design-and-ux/responsive/) when you're first starting out (mobile and tablet). Just focus on the Desktop dispay to start out. Once you have a firm grasp of writing CSS you can look into making the site responsive. So for now, ignore the screenshots with `(mobile)` and `(tablet)`.

2. Work on one section at a time. Don't get overwhelmed by feeling the need to make the entire site look correct immediately.

3. The HTML is already provided, but don't feel locked into it. You can alter it however you need. However, it is already 95% of what you need. The majority of the time you just need to add CSS classes.

4. Ignore Javascript for now and just focus on the design. Basic CSS interactions can be added when you are finished such as transitions and hovers.

5. The only CSS class already provided is a `l-container` class which is used to bring the text in off the sides of the screen. This class is often applied inside of a `<section>` so that the section can go full-width. This allows styles like the background color to be full-width while all the text stays aligned inside the container.

> __Hint:__ the `l-` prefix on the `l-container` class is used to signify that this class should only be used for Layout. Don't apply other styles to this class like colors or fonts. It's sole purpose is for layout positioning.


## Google Fonts

Google Fonts https://fonts.google.com/ are used to style the text on the page. Below are the fonts needed for their appropriate sections.

* __Headings:__ "Playfair Display", serif;
* __Paragraph:__ "Open Sans", sans-serif;

# CSS Pro Tips
There are many ways to structure CSS. Do whatever way you have learned. However, here are some things to consider based off of years of using CSS in small one-page sites all the way to massive enterprise sites.

1. ID selectors (ex. `#something`) should __NEVER__ be used! Only use classes. https://csswizardry.com/2011/09/when-using-ids-can-be-a-pain-in-the-class/

2. Use the __BEM__ (`Block`, `Element`, `Modifier`) naming convention. Yes, it might be a little weird to look at, but it keeps all your components scoped so that styles don't leak out into other areas of the site. It also keeps the structure "Flat" so that you don't run into specificity issues within the cascade.
    * [http://csswizardry.com/2013/01/mindbemding-getting-your-head-round-bem-syntax/](http://csswizardry.com/2013/01/mindbemding-getting-your-head-round-bem-syntax/)
    * [https://css-tricks.com/bem-101/](https://css-tricks.com/bem-101/)

```css
.block {
  /* The main component styles. */
}
 
.block__element {
  /* Style a "thing" that is part of the component. */
}
  
.block--modifier {
  /* Styles that alter or change pre-existing "things". */
}
```

3. If you aren't using __BEM__, you should still do your best to keep your CSS as "Flat" as possible. Stay away from long selectors like `body header .main-menu > ul > li a`. I promise that selectors like this will come back to bite you. Instead just drop a class directly onto that `a` tag and target the class directly. You shouldn't need more than one or two parent selectors. Better if none at all.

4. Don't tie your CSS to the HTML structure. Just because you have a `div` inside a `div` inside a `div` in your HTML doesn't mean your CSS needs to match that with `div > div > div`. Just drop a class on your last `div` and target the class.

5. Just use classes! Notice a recurring theme here? That's all you need. Do your best to stay away from selectors that include HTML like `nav.main-menu`. Just do `.main-menu`.



# Credits

This code is adapted from the Akame template created by [ColorLib](https://colorlib.com)

* __Template Name:__ Akame - Hair Salon HTML Template
* __Author:__ Colorlib
* __Author URI:__ https://colorlib.com/wp/template/akame/
* __Released:__ February, 2019
* __Licence:__ CC BY 3.0
* __Images:__ From Unsplash https://unsplash.com/
