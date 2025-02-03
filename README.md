# CSS Specificity Bug: Unexpected Color Inheritance

This repository demonstrates a subtle bug related to CSS selector specificity and the cascading order. The bug arises from an unexpected color inheritance that contradicts intuitive expectations.

## Bug Description

The provided CSS code includes rules that define styling for a container and paragraphs within it.  A nested `.inner` class further complicates the styling. The bug lies in the unexpected color of the paragraph nested within the `.container .inner`. The CSS specificity rules lead to unexpected inheritance, causing the paragraph to not inherit the color from the most specific rule.

## How to Reproduce

1. Clone this repository.
2. Open `bug.css` to examine the CSS code.
3. Create an HTML file with a matching structure. For instance:
   ```html
   <div class="container">
     <p>This is a paragraph.</p>
     <div class="inner">
       <p>This is a nested paragraph.</p>
     </div>
   </div>
   ```
4. Link `bug.css` to your HTML file.
5. Observe that the nested paragraph inherits an unexpected color due to specificity and cascading rules.

## Solution

The solution involves adjusting the CSS rules to ensure the desired style is applied.  See `bugSolution.css` for the corrected code.

## Lessons Learned

This example highlights the importance of understanding CSS specificity and the cascading order to prevent unexpected styling behaviors. Carefully considering the specificity of selectors and the order in which they appear in the stylesheet is crucial for maintaining predictable and consistent styling.