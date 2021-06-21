# Separate Content and Appearance

## Reduce Redundancy

- Using classes and IDs helps decrease the redundant usage of styling attributes. In developing there is a concept called DRY (Don’t Repeat Yourself) and it juxtaposes WET (Write Everything Twice, or Waste Everyone’s Time). Make sure you keep your code as lean as possible. It will benefit everyone involved.

### Choose Tags Wisely

\_\_

## BEM Naming

- BEM stands for ‘Block Element Modifier’ and is used to structure and organize your class names.

            A Block is a distinct part of a web page and groups a series of elements; it
            forms the base name for the class (.block).

            An Element is a child item of a block and has two underscores to separate it from
             the block name (.block__element).

            A Modifier changes a block or element based on specific circumstances and is separated
            by two hyphens (.block—modifier or .block__element—modifier).

             <ul class=”navbar”>
                  <li class=”navbar__item--active”>
                      <a>Home</a>
                  </li>
                  <li class=”navbar__item”>
                      <a>About</a>
                </li>
                <li class=”navbar__item”
                     <a>Contact</a>
              </li>
                  </ul>


                  <div class=”gallery”>
                        <img class=”gallery_image” />
                        <img class=”gallery_image” />
                        <img class=”gallery_image—selected” />
                  </div>

#### Here are a few benefits of using BEM:

> BEM blocks are re-useable

- Block styles are never dependent on other elements
- It is easy to transfer BEM blocks from one project to another
