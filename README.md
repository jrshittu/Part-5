# Part-5
## Contents
[Custom properties and variables](#custom)
[CSS Frameworks](#frame)
[Project 1](#pro1)
[Project 2](#pro2)
[Project 3](#pro3)
[References and Resources](#ref)

## CSS Custom Properties and Variables:
**CSS custom properties (aka CSS variables or cascading variables)** allow you to store and reuse values throughout your stylesheet.They act as placeholders for values that can be easily changed in one place, affecting all styles that use them.

**Benefits:**

- **Maintainability:** Reduce code duplication and make your styles more organized and easier to update.
- **Themeability:** Easily switch between different themes by changing only the values of custom properties.
- **Dynamic styles:** Create dynamic styles that react to user interaction or browser features using JavaScript.

**How to use them:**

1. **Declare the custom property:**
    - Using two dashes as a prefix (`--variable-name: value;`)
    - Using the `@property` at-rule (`@property --variable-name { syntax: <value-type>; initial-value: value; }`)
2. **Use the `var()` function** to access the value (`background-color: var(--primary-color);`)

**Key points:**

- Custom properties are **scoped** to the element(s) they are declared on and participate in the cascade.
- They can be used to store all types of CSS values, including colors, lengths, fonts, and even complex calculations.
- Values can be **overridden** by declarations with higher specificity.
- JavaScript can be used to access and modify custom properties dynamically.

## Use Case: Theme Switching with CSS Custom Properties

Imagine you're building a website with two distinct themes: light and dark. You want to make it easy for users to switch between these themes on the fly.

**Without Custom Properties:**

You would need to duplicate your entire stylesheet, replacing all the color values for each theme. This would lead to a lot of code duplication and make it difficult to maintain.

**With Custom Properties:**

1. Define custom properties for your primary colors:

```css
--primary-color: #222222;
--secondary-color: #ffffff;
--background-color: #eee;
--text-color: #222;
```

2. Use these custom properties throughout your stylesheet:

```css
body {
  background-color: var(--background-color);
  color: var(--text-color);
}

h1 {
  color: var(--primary-color);
}

a {
  color: var(--secondary-color);
}
```

3. Create buttons or a toggle to switch the values of the custom properties:

```html
<button onclick="document.body.style.setProperty('--primary-color', '#ffffff'); document.body.style.setProperty('--secondary-color', '#222222');">Switch to Light Theme</button>
```

By changing the values of just these four custom properties, you can instantly switch the entire theme of your website. This demonstrates the power and flexibility of CSS custom properties.

## CSS Frameworks
CSS frameworks are pre-built collections of CSS styles that provide a solid foundation for web development. They offer pre-defined styles for common elements like buttons, forms, and grids, saving you time and effort.

**Benefits:**

- **Faster development:** Jumpstart your project with ready-made styles and components.
- **Consistency:** Ensure consistent design across your website.
- **Responsiveness:** Many frameworks provide responsive design features, making your website look good on all devices.
- **Community and resources:** Access a large community of developers and extensive documentation for support.

**Popular Frameworks:**

- **Bootstrap:** Widely used, mobile-first framework with a vast library of components.
- **Tailwind CSS:** Utility-first framework for building custom designs with low-level classes.
- **Material Design:** Google's framework based on their design principles, offering a clean and modern aesthetic.
- **Foundation:** Flexible framework with a focus on accessibility and modularity.
- **Bulma:** Lightweight and minimalist framework with a focus on simplicity.

**Choosing a Framework:**

Consider your project needs, desired level of customization, and team experience when choosing a framework.

**Key Points:**

- Frameworks can simplify development but may add complexity and bloat to your code.
- Learn the framework's core principles to leverage its full potential.
- Customize the framework to suit your specific needs and brand identity.

**Resources:** <a name="ref"></a>

- **MDN Web Docs:** [https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_custom_properties](https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_custom_properties)
- **W3Schools:** [https://www.w3schools.com/css/css3_variables.asp](https://www.w3schools.com/css/css3_variables.asp)
- **GitHub Pages Sample:** [https://ucsb-meds.github.io/customizing-websites-css/](https://ucsb-meds.github.io/customizing-websites-css/)
- **Comparison of CSS frameworks:** [https://css-tricks.com/considerations-for-making-a-css-framework/](https://css-tricks.com/considerations-for-making-a-css-framework/)
- **A Beginner's Guide to CSS Frameworks:** [https://www.freecodecamp.org/news/best-css-and-css3-tutorial/](https://www.freecodecamp.org/news/best-css-and-css3-tutorial/)
