# What I Learned In Week 2 at Code Immersives
1. **Learnt about Grid**
   A grid is a set of intersecting horizontal and vertical lines defining columns and rows. Elements can be placed onto the grid within these column and row lines 
   ![alt Markdown Vs HTML](https://codingthesmartway.com/wp-content/uploads/2017/12/01_CSS_Grid_Overview.png)
   

2. **How to make a div a grid**
   - In css file we have to make the div's property display to **grid**.
   ```css
   .wrapper {
    display: grid;
   }
   ``` 

3. **Size of rows and columns in a grid**
   ##### Size of row and columns in a grif can be fixed or/and flexible. 
     1. Fixed sizes are according to the specified pixel e.g 200px
     2. Flexible sizes are with percentages or with the new fr unit designed for this purpose eg  1fr , 20%

4. **How to define rows and columns in grid**
  ##### We define rows and columns in our grid with the grid-template-columns and grid-template-rows properties.
     1. 
     ```css
     .wrapper {
      display: grid;
      grid-template-columns: 200px 200px 200px;
      }
      ```

     2.
      ```css
     .wrapper {
     display: grid;
     grid-template-columns: 200px 200px 200px;
     grid-template-rows: 1fr 1fr 1fr;
     }
     ```
     This will make a grid of 3 columns of 200px each and 3 rows each of which will take 1/3 height of the grid.

5. **Positioning items against line**
 ##### By using the following properties of grid item we can position an item anywhere in the grid.
   1. grid-column-start
   2. grid-column-end
   3. grid-row-start
   4. grid-row-end

Determines a grid item’s location within the grid by referring to specific grid lines. grid-column-start/grid-row-start is the line where the item begins, and grid-column-end/grid-row-end is the line where the item ends.

6. **Grid-column and Grid-row**
Shorthand for grid-column-start + grid-column-end, and grid-row-start + grid-row-end, respectively.
```css
 .item {
  grid-column: 3 / 5; (starts from column 3 and ends at the beginning of column 5)
  grid-row: 1 / 4;(starts from row 1 and ends at the beginning of row 4)
}
```

6. **Span**
 ##### span <number> – the item will span across the provided number of grid tracks
```css
 .item-c {
  grid-column: 3 / span 2;(starts from column 3 and ends at the beginning of column 5)
  }
  ```
   ##### This is equal to  
  ```css 
  .item-c {
  grid-column: 3 / 5;
  }
  ```
  
  

7. **Grid-template-areas**
 ##### Defines a grid template by referencing the names of the grid areas which are specified with the grid-area property. Repeating the name of a grid area causes the content to span those cells. A period signifies an empty cell. The syntax itself provides a visualization of the structure of the grid.
    1. defining grid structure
    ```css
    .container {
       display: grid;
       grid-template-columns: 50px 50px 50px 50px;
       grid-template-rows: auto;
       grid-template-areas: 
                "header header header header"
                "main main . sidebar"
                "footer footer footer footer";
               }
    ```

    2. defining item the name of grid-area assign to it
    ```css
    .item-d {
      grid-area: header;
    }
    ```
    
   
8. **Align-self**
 ##### Aligns a grid item inside a cell along the block (column) axis.

9. **Justify-self**
 ##### Aligns a grid item inside a cell along the inline (row) axis.
    
10. **Wire frame**
 ##### Wire frame is an outline of a webpage or app. It provide a clear overview of the page structure. This process allows all stakeholders to agree on where the information will be placed before the developers build the interface out with code.
 ![alt Markdown Vs HTML](https://miro.medium.com/max/800/1*ZvtdfRPAdFpf2av_bvqE6w.png)
 