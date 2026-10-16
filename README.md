# Tailwind Notes

## Setup
- Add the script tag in the `<head>`. No CSS file needed. 
- Tailwind resets the browser deafaults. 

## Utility classes
- Every Tailwind class = one css declaration.
- `bg-teal-700` = background-color. `text-white` = color.
- The styles go in the `class`, not in a CSS file. 

## Scales
- Spacing number x 4 = pixels `p-6` = 24px.
- `p` = all sides, `px` = leftRight, `py` = top&bottom, `pt` = top only. 

## Hover
- `hover: ` = only while the mouse is over it. 
- `transition` = fade the change in smoothly.
- A prefix says when a class applies. 

## Text on top of an image
- Outer box: `relative` + a height (`h-64`).
- Image: `absolute inset-0 w-full h-full object-cover` = out of the flow, stretched top the edges of Outer box
- Dark layer: `abosolute inset-0 bg-black/50` (black at 50% opacity).
- Text: `relative`, and it comes last in the HTML so it's drawn on top

# Responsive Notes

## Breakpoints
- `md:grid-cols-3` = at 750px and up. A floor, not a range
- No prefix = always, even on the smallest screen. 
- sm: 640, md: 768, lg: 1024, xl: 1280. 

## More than columns
- `p-4 md: p-6` = less padding on phones, more one bigger screens. 
- `text-2xl md:text-3xl` = smaller headings on phones. 
- `hidden md:block` = hidden on phones, shown at 768px and up. 
- `hidden` removed if for screen readers as well. DO NOT hide anything too important. (links, unique info). 

## Media queries
- `@media (min-width: 768px){ ... }` = only at 768px and up. 
- `md:` is a media query that TailWind writes for us. 

## Responsive header
- `flex flex-col md:flex-row` = stacked on phones, side by side at 768px and up.
