#### $\textcolor{red}{\textsf{Color didint work .}}$

#### $\textcolor{green}{\textsf{Color didint work .}}$

$${\color{green}Preview\ text}$$

$\color{#D29922}\textsf{\Large\&#x26A0;\kern{0.2cm}\normalsize Warning}$ 
$\color{#58A6FF}\textsf{\Large\&#x24D8;\kern{0.2cm}\normalsize Note}$

$foo$
$lorem ipsum dolor sit amet$

**$\text{lorem ipsum dolor sit amet}$**

**$\textbf{lorem ipsum dolor sit amet}$**

$\textbf{lorem ipsum dolor sit amet}$

$hello$
`$\fcolorbox{yellow}{red}{\textsf{lorem ipsum}}$`

### $\textcolor{green}{\textsf{Best Practice&nbsp; -------------------}}$ $\textcolor{red}{\textsf{------------Bad Practice}}$

&nbsp;
#### 2. Always prioritise on using predefined utility class which is either provided by mixins or common styles

### $\textcolor{green}{\textsf{Best Practice}}$		
``` Scss
Scss:
.font-size-12 {
  font-size: 12px; 
}
```
```html
HTML:
<p class=”font-size-12”>Hello</p>
<p class=”font-size-12”>World</p>
```


### $\textcolor{red}{\textsf{Bad Practice}}$
	Scss
	.font-size-12 {
	&nbsp; &nbsp; font-size: 12px;
	}
	.world-text {
	&nbsp; &nbsp; font-size: 12px;
	}
	Html
	`<p class=”font-size-12”>Hello</p>`
	`<p class=”world-text”>World</p>`
	{.is-danger}

> <span style="color:#FF0000">Using explicit scss or css even when there are utility classes will cause you the fine below</span>
><span style="color:#FF0000; font-size: 24px;">CSS-002: Nu. 20</span>
{.is-info}

&nbsp;
#### 3. For `padding, margin and font-size`, let’s follow` multiples of 4 or 2 `and as far as possible, avoid using negative margin.

		> **Best Practice**
		h1 {
		&nbsp; &nbsp; font-size: 24px: 
		} 
		h2 {
		&nbsp; &nbsp; font-size: 24px;
		}
		.p-4 {
		&nbsp; &nbsp; padding: 4px;
		}
		.p-8 {
		&nbsp; &nbsp; padding: 8px;
		}
		.m-4 {
		&nbsp; &nbsp; margin: 4px;
		}
		.m-8 {
		&nbsp; &nbsp; margin: 8px;
		}
		> {.is-success}

> **Bad Practice**
	h1 {
 	&nbsp; &nbsp; font-size: 35px: 
 	}
  h2 {
   &nbsp; &nbsp; font-size: 23px;
  }
  .p-5 {
   &nbsp; &nbsp; padding: 5px;
  }
  .p-6 {
   &nbsp; &nbsp; padding: 6px;
  }
  .m-7 {
   &nbsp; &nbsp; margin: 7px;
  }
  .m-8 {
   &nbsp; &nbsp; margin: 9px;
  }
{.is-danger}

> <span style="color:#FF0000">There will be certain exceptions but given that positive or multiples of 2 or 4 could have been used, you will be fined</span> 
<span style="color:#FF0000; font-size: 24px;">CSS-003: Nu. 20</span>
{.is-info}


&nbsp;
#### 4. Avoid giving inline css to an html tag. Instead give a proper css class
> **Best Practice**
	Scss
 .font-size-16 {
 	&nbsp; &nbsp; font-size: 16px;
 }
 Html
 `<div class=”font-size-16”></div>`
> {.is-success}

> **Bad Practice**
  `<div style=”font-size:16px”>`
{.is-danger}


> <span style="color:#FF0000">There will be certain exceptions but given that inline could have been avoided, you will be fined.</span>
> <span style="color:#FF0000; font-size: 24px">CSS-004: Nu. 20</span>
{.is-info}


&nbsp;
#### 5. Make best use of shorthand property
Refer: https://developer.mozilla.org/en-US/docs/Web/CSS/Shorthand_properties
Generator: https://shrthnd.volume7.io/

 
> **Best Practice**
	Scss
  p {
    &nbsp; &nbsp; margin: 4px;
    &nbsp; &nbsp; background: #000 url(‘images/bg.gif’) no-repeat left top;
  }
  .info {
    &nbsp; &nbsp; margin: 4px 8px;
  }
  .card-layout {
    &nbsp; &nbsp; margin: 16px 4px 8px;
  }
> {.is-success}

> **Bad Practice**
  p {
    &nbsp; &nbsp; margin-left: 4px;
    &nbsp; &nbsp; margin-right: 4px;
    &nbsp; &nbsp; margin-top: 4px;
    &nbsp; &nbsp; margin-bottom: 4px;
    &nbsp; &nbsp; background-color: #000;
    &nbsp; &nbsp; background-image: url(‘images/bg.gif’);
    &nbsp; &nbsp; background-repeat: no-repeat;
    &nbsp; &nbsp; background-position: left top;
  }
  .info {
    &nbsp; &nbsp; margin-left: 4px;
    &nbsp; &nbsp; margin-right: 4px;
    &nbsp; &nbsp; margin-top: 8px;
    &nbsp; &nbsp; margin-bottom: 8px;
  }
  .card-layout {
   	&nbsp; &nbsp; margin-left: 4px;
    &nbsp; &nbsp; margin-right: 4px;
    &nbsp; &nbsp; margin-top: 16px;
    &nbsp; &nbsp; margin-bottom: 8px;
  }
{.is-danger}
 
 > <span style="color:#FF0000; font-size: 24px;">CSS-005: Nu. 20</span>
{.is-info}

 &nbsp;

#### 6. Use specific property for background unless all properties are covered in the shorthand property.
-for background image use background-image.
-for background color use background-color.

add example.

 &nbsp;
#### 7.For helper classes let’s not use `!important` because it should be overwrite-able

> **Best Practice**
	body {
    &nbsp; &nbsp; font-family: Arial;
    &nbsp; &nbsp; overflow-x: hidden;
    &nbsp; &nbsp; font-size: 14px;
  }
  h1 {
    &nbsp; &nbsp; font-size: 28px;
  }
> {.is-success}

> **Bad Practice**
  body {
   &nbsp; &nbsp; font-family: Aria !important;
   &nbsp; &nbsp; overflow-x: hidden !important;
   &nbsp; &nbsp; font-size: 14px !important;
  }
  h1 {
   &nbsp; &nbsp; font-size: 28px !important;
  }
{.is-danger}

> <span style="color:#FF0000">There will be certain exceptions but given that this could have been avoided, you will be fined</span> 
> <span style="color:#FF0000; font-size: 24px;">CSS-006: Nu. 20</span>
{.is-info}

&nbsp;
#### 8. Always look for an alternative other than using `position:absolute`. It’s convenient to use that but it would cause issues that we never imagined.

> **Best Practice**
	***Use flex or float for alignment***
	Example:
  &nbsp;&nbsp; float: right;
  &nbsp;&nbsp; align-self: auto | flex-start | flex-end | center | baseline | stretch;
> {.is-success}

> **Bad Practice**
  .profile-img {
   &nbsp; &nbsp; position: absolute;
   &nbsp; &nbsp; right: 0 !important;
  }
{.is-danger}

> <span style="color:#FF0000">There will be certain exceptions but given that this could have been avoided, you will be fined</span>
> <span style="color:#FF0000; font-size: 24px">CSS-007: Nu. 50</span>
{.is-info}

&nbsp;
#### 9. Use `Single Quote` for all urls and contents (Refer Onboarding steps)

> **Best Practice**
	.container {
  &nbsp;&nbsp; background-image: url('images/logo.png');
  &nbsp;&nbsp; content: 'hello';
  }
> {.is-success}

> **Bad Practice**
  .container {
  &nbsp;&nbsp; background-image: url("images/logo.png");
  &nbsp;&nbsp; content: "hello";
  }
{.is-danger}


> <span style="color:#FF0000; font-size: 24px;">CSS-008: Nu. 10</span>
{.is-info}

&nbsp;
#### 10. Make best use of `cal()` function along with vh and vw instead of static pixels. 
Refer: https://www.sitepoint.com/css-viewport-units-quick-start/

> **Best Practice**
	.plot {
  &nbsp;&nbsp; width: calc(100vw - 100px);
  &nbsp;&nbsp; height: 100vh;
  }
> {.is-success}

> **Bad Practice**
  .plot {
  &nbsp;&nbsp; width: 1000px;
  &nbsp;&nbsp; height: 900px;
  }
  @media (min-width: 600px) {
  &nbsp;&nbsp; .plot {
  &nbsp; &nbsp;&nbsp;  width: 600px;
  &nbsp; &nbsp;&nbsp;  height: 700;
  }
  @media (max-width: 599px) {
  &nbsp;&nbsp; .plot {
  &nbsp; &nbsp;&nbsp;  width: 500px;
  &nbsp; &nbsp;&nbsp;  height: 600px;
  }
{.is-danger}
 

&nbsp;
#### 11. Use `Clearfix` to avoid HTML element jam
Refer: https://css-tricks.com/clearfix-a-lesson-in-web-development-evolution/

add eg

&nbsp;
#### 12. Border radius should be uniform components with edges like buttons and cards according to style guidelines.

> **Best Practice**
	button, .card {
  &nbsp;&nbsp; border-radius: 4px;
  }
> {.is-success}

> **Bad Practice**
  button {
  &nbsp;&nbsp; border-radius: 10px;
  }
  .card {
  &nbsp;&nbsp; border-radius: 4px;
  }
{.is-danger}




# HTML
#### 1. HTML Hierarchy
Refer: https://medium.com/ux-art/html-hierarchy-tree-7a2947f2bf01

- Let’s avoid declaring `<p>` inside any `<button>` etc
  
```html
Best Practice																						Bad Practice
1. <button mat-button color="primary>										1. <button mat-button color= "primary">
	  Login																									  	<p>Login</p>
   </button>  																					    </button>   

2. <p>   																								2. <p> 
	  Hello																										Hello
    <span>World</span>																       <div>World</div>
   </p>                                                    </p>
```

> <span style="color:#FF0000">By any means we have to follow HTML hierarchy</span>
> <span style="color:#FF0000; font-size: 24px">HTML-001: Nu. 20</span>
{.is-info}

&nbsp;
#### 2. Always give alt attribute with an `<img>` tag
- Please add height and width in the image tag.
- Use underscore (_) for naming images.
- Please add proper descriptive text with proper sentence formatting.
```html
Best Practice																																
<img src=”../../../assets/images/profile_image.jpg” alt=”Profile Image” width="400px" height="400px"/>

Bad Practice
<img src=”../../../assets/images/profile-image.jpg”>
<img src=”../../../assets/images/profile.jpg” alt="Profile.jpg">
																																							
```
> <span style="color:#FF0000">All images should have alt attribute with proper text which is not repetitive</span>
> <span style="color:#FF0000; font-size: 24px;">HTML-002: Nu. 10</span>
{.is-info}

&nbsp;
#### 3. Always compress file size of assets to not hamper load time
*Recommendation for image resize files:* 
1. Figma
2. Photoshop
		
		
> <span style="color:#FF0000">If image is not compressed and still in KB</span>
> <span style="color:#FF0000; font-size: 24px;">HTML-003: Nu. 20</span>
{.is-info}


> <span style="color:#FF0000">If Image is in MB</span>
> <span style="color:#FF0000; font-size: 24px;">HTML-004: Nu. 50</span>
{.is-info}


&nbsp;
#### 4. Same design needed in multiple placeholder
- If the same design is required in multiple placeholders, let’s create directive or a component template for it, so that we can maintain clean codes as well as it will be convenient to modify in future.

> <span style="color:#FF0000">There will be certain exceptions but given that this could have been avoided, you will be fined</span>
> <span style="color:#FF0000; font-size: 24px;">HTML-005: Nu. 20</span>
{.is-info}

&nbsp;
#### 5. Loop Over the classes or elements that have the same properties.

```html
Best Practice														            
<mat-card *ngFor="let item of items">{{item}} </mat-card> 

Bad Practice
<mat-card> </mat-card> 								  
<mat-card> </mat-card>
<mat-card> </mat-card>
<mat-card> </mat-card>
```
> <span style="color:#FF0000; font-size: 24px;">HTML-006: Nu. 20</span>
{.is-info}


&nbsp;
#### 6. Use of HTML entity
- Use html entity for cases like copyright instead of special characters.
> **Best Practice**
 `&copy` copyright, All rights reserved.
> {.is-success}

> **Bad Practice**
 ***Do not copy paste and use***
  © copyright, All rights reserved.
{.is-danger}

- Bind currentYear in FE and BE both

> **Best Practice**
  ***Angular***
  &nbsp; ts: year = new Date().getFullYear();
  &nbsp; HTML: Company Name {{year}}, All rights reserved. 
  ***Rails***
  &nbsp; Company Name <%= DateTime.now.year %>, All rights reserved.
 > {.is-success}

> **Bad Practice**
  Company Name 2020, All rights reserved.
{.is-danger}


> <span style="color:#FF0000; font-size: 24px;">HTML-007: Nu. 20</span>
{.is-info}

&nbsp;
#### 7.Carelessness
```html
Best Practise                              			 Bad Practice 
<p> Hello </p>											 						 <P> Hello </P>
<div> Lorem Ipsum </div>								 				 <DIV> Lorem Ipsum </div>
```

>  <span style="color:#FF0000; font-size: 24px;">HTML-008: Nu.50 </span>
{.is-info}

&nbsp;
#### 8. HTML Lines  of code
- html lines of code should not be more than (yet to discuss)


&nbsp;
#### 9. Proper Indentation of code. Use predefined HTML selectors for better segregation and understandability with proper indentation

> **Best Practice**
  *Good code understandability* (add better example)
  ![screen_shot_2020-06-24_at_2.27.09_pm.png](/ui-conventions/screen_shot_2020-06-24_at_2.27.09_pm.png)
> {.is-success}

> **Bad Practice**
 *No proper understandability of the code*
![screen_shot_2020-06-24_at_3.10.43_pm.png](/ui-conventions/screen_shot_2020-06-24_at_3.10.43_pm.png)
{.is-danger}


&nbsp;
#### 10. We need to start using html5 tags since these help us in understandability. It also helps in SEO.

```html
Best Practice
<html>
<body>
 <header></header>
 <aside></aside>
 <section>
     <article></article>
 </section>
  <section></section>
  <footer></footer>
</body>
</html>
 ```

&nbsp;
#### 11.If there are more than one images, let's group them inside the `<figure>` tag.

```html
Best Practice																														Bad Practice
<figure>																													 		
  <img src=”../../../assets/images/test1jpg” alt=”Profile Image” ...>			  	<img src=”../../../assets/images/test1jpg” alt=”Profile Image”>
 <img src=”../../../assets/images/test2.jpg” alt=”Profile Image” ...>		 	  <img src=”../../../assets/images/test2.jpg” alt=”Profile Image”>
 <img src=”../../../assets/images/test3.jpg” alt=”Profile Image” ...>				  <img src=”../../../assets/images/test3.jpg” alt=”Profile Image”>
</figure>																													  	
```

&nbsp;
#### 12. Use of Default Images
Storing dummy images locally are not allowed, instead use default images. If using cdn links for images, then generate the link from Assets Manager. <a href="https://selise.assets.selise.club/" target="_blank">Click here</a> to generating the link

> <span style="color:#FF0000">If found storing dummy images</span>
> <span style="color:#FF0000; font-size: 24px;">HTML-009: Nu. 30</span>
{.is-info}

# SCSS

#### 1. Stylesheet filename should always use `hyphen` between 2 words. Use max 2 words only. Avoid obvious terms like styles

> **Best Practice**
 `_fonts.scss`
 `_utility.scss`
 `_font-size.scss`
 `_overwrite.scss`
 All the above compiled in style.scss
> {.is-success}

> **Bad Practice**
  1.Including all the styles in style.scss.
  2.File named as font-size.scss or media-query-mixin.scss
{.is-danger}

> <span style="color:#FF0000">Basic SCSS</span>
> <span style="color:#FF0000; font-size: 24px;">SCSS-001: Nu. 30</span>
{.is-info}

&nbsp;
#### 2. Define Variables for colors always 
- Try to use material template color variables if using material UI.
- Always use 6 digit/character's HEX value in CAPITAL letters.
- Always use 3 DIGIT decimal value for alpha in rgba value 
- Update stylelint (add screenshot)

> **Best Practice**
 *Variable*
 $black: #000000;
 p {
  &nbsp;&nbsp;color: $black;
 }
 .info-text {
  &nbsp;&nbsp;color: $black;
 }
 .black-70 {
  &nbsp;&nbsp;color: rgba( $black, 0.70 );
 }
> {.is-success}

> **Bad Practice**
*Including all the styles in style.scss* 
 p {
  &nbsp;&nbsp;color:  #000;
 }
 .info-text {
  &nbsp;&nbsp;color: #000000;
 }
 .black-7 {
  &nbsp;&nbsp;color: rgba( $black, 0.7 );
 }
{.is-danger}

> <span style="color:#FF0000">DO NOT use the hex value directly in your scss..</span>
> <span style="color:#FF0000; font-size: 24px;">SCSS-002: Nu. 30</span>
{.is-info}

&nbsp;
#### 3. Do not define variables for rgba colors. Use sass functionality instead

* No more having multiple shades of gray each time a new color is given in our specs.We only use the existing colors we have defined (We can discuss and add up the colors which we have used most commonly all over our projects).

> **Best Practice**
 *Variable*
 `$black: #000000;`
 p {
  &nbsp;&nbsp;color:  rgba($black, 0.70);
 }
> {.is-success}

> **Bad Practice**
 $black: #000000;
 $black-07: rgba(0,0,0,0, 0.7);
 $black-87: rgba(0,0,0,0, 8.7);
 p {
  &nbsp;&nbsp;color:  $black-07;
 }
 .info-text {
  &nbsp;&nbsp;color: $black-87;
 }
{.is-danger}

> <span style="color:#FF0000">Unnecessary shades of any colors will be fined.</span>
<span style="color:#FF0000; font-size: 24px;">SCSS-003: Nu. 20</span>
{.is-info}

&nbsp;
#### 4. Media queries should be within the same class instead of separate general device queries.

> **Best Practice**
 .header {
  &nbsp;&nbsp; width: 1000px;
  &nbsp;&nbsp; @media (max-width: 350px) {
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; width: 120px;
   &nbsp;&nbsp;&nbsp;&nbsp; }
   &nbsp;&nbsp; @media (max-width: 980px) {
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; width: 320px;
   &nbsp;&nbsp;&nbsp;&nbsp; }
  }
  }
> {.is-success}

> **Bad Practice**
  .header {
  &nbsp;&nbsp; width: 1000px;
  }
  @media (max-width: 350px) {
  .header {
      &nbsp;&nbsp;&nbsp;&nbsp; width: 120px;
      }
  }
  @media (max-width: 980px) {
  .header {
      &nbsp;&nbsp;&nbsp;&nbsp; width: 320px;
      }
  }
{.is-danger}

> <span style="color:#FF0000">For better readability it's always better to include all the media queries wrapped within the particular element or class.</span>
> <span style="color:#FF0000; font-size: 24px;">SCSS-004: Nu. 40</span>
{.is-info}


&nbsp;
#### 5. If same styling is to be applied in multiple classes then use `sass @extend`

> **Best Practice**
Example 1 (@extend with placeholder selector)
 %button-basic  {
  &nbsp;&nbsp; padding: 12px 20px;
  &nbsp;&nbsp; text-align: center;
  &nbsp;&nbsp; font-size: 16px;
  &nbsp;&nbsp; text-transform: uppercase;
  &nbsp;&nbsp; cursor: pointer;
}
 .button-report  {
  &nbsp;&nbsp; @extend %button-basic;
  &nbsp;&nbsp; background-color: red;
}
.button-submit  {
  &nbsp;&nbsp; @extend %button-basic;
  &nbsp;&nbsp; background-color: green;
  &nbsp;&nbsp; color: white;
}<br>
Example 2 (@extend with class selector)
 .button-basic  {
  &nbsp;&nbsp; padding: 12px 20px;
  &nbsp;&nbsp; text-align: center;
  &nbsp;&nbsp; font-size: 16px;
  &nbsp;&nbsp; text-transform: uppercase;
  &nbsp;&nbsp; cursor: pointer;
}
 .button-report  {
  &nbsp;&nbsp; @extend .button-basic;
  &nbsp;&nbsp; background-color: red;
}
.button-submit  {
  &nbsp;&nbsp; @extend .button-basic;
  &nbsp;&nbsp; background-color: green;
  &nbsp;&nbsp; color: white;
}
> {.is-success}

> **Bad Practice**
 .button-report  {
  &nbsp;&nbsp; padding: 12px 20px;
  &nbsp;&nbsp; text-align: center;
  &nbsp;&nbsp; font-size: 16px;
  &nbsp;&nbsp; text-transform: uppercase;
  &nbsp;&nbsp; cursor: pointer;
  &nbsp;&nbsp; background-color: red;
}
.button-submit  {
  &nbsp;&nbsp; padding: 12px 20px;
  &nbsp;&nbsp; text-align: center;
  &nbsp;&nbsp; font-size: 16px;
  &nbsp;&nbsp; text-transform: uppercase;
  &nbsp;&nbsp; cursor: pointer;
  &nbsp;&nbsp; background-color: green;
  &nbsp;&nbsp; color: white;
}
{.is-danger}

> <span style="color:#FF0000">Repetition will be fined</span>
> <span style="color:#FF0000; font-size: 24px;">SCSS-005: Nu. 20</span>
{.is-info}

&nbsp;
#### 6. Basic CSS/SCSS typos or combinations missed

> **Best Practice**
 .container, .profile {
   &nbsp;&nbsp; width: 100%;
 }
> {.is-success}

> **Bad Practice**
 .container {
   &nbsp;&nbsp; width: 100%;
 }
 .profile {
   &nbsp;&nbsp; width: 100%;
 }
{.is-danger}

> <span style="color:#FF0000; font-size: 24px;">SCSS-006: Nu. 50</span>
{.is-info}


&nbsp;
#### 7. Copied Codes not removed
add better example
```html
Best Practise                                            				   Bad Practice 
<table mat-table>   																							 <table mat-table>
	<th mat-header-cell> Weight </th> 																 <!--Note that these columns can be defined in any order. -->	 		 
  <td mat-cell> {{element.weight}} </td>	                           <!--Name Column--> 
</table>																														 <th mat-header-cell> Weight </th>
                                                                     <td mat-cell> {{element.weight}} </td>		
                                                                    <table>  
```
>  <span style="color:#FF0000; font-size: 24px;">SCSS-007: Nu.30</span>
{.is-info}

&nbsp;
#### 8. Provide the stylesheet info by commenting
- recommended for mixins

```scss
Best Practice
_variables.scss
/*
Variables.scss: contains variables referable by other stylesheet to avoid redundancy 
*/
```

&nbsp;
#### 9.Always write (&:hover, &:focus) intact and give pointer cursor to all action links and buttons

```css
a {
	 text-decoration: none;
   &:hover, &:focus {
       cursor: pointer
  }
}
```

&nbsp;
#### 10. Let us avoid using long path names while importing

> **Best Practice**
 @import ‘variables’
> {.is-success}

> **Bad Practice**
 @import ‘../../assets/stylesheets/variables’
{.is-danger}

example of config: 

add here 

&nbsp;
#### 11. Always install SCSS lint plugin in webstorm or any other IDE you are using
-To be discussed further


# Framework 
## React 

### 1. File Naming Conventions
* A folder and sub folder names should always start with small letters and the function name should always be in the PascalCase (i.e, First letter of the component name with capital letter).
* Name of the folder and sub folder name  should be always separated by  “-”. 
* Avoid using “_” and avoid direct naming the folder and sub folder with “PascalCase”.
> **Best Practice**
  ![1.png](/ui_react/1.png)
> {.is-success}

&nbsp;
### 2. Structuring Folder

* All the components, globals, shared components,  assets, translation,  redux etc.. Should be written inside the app folder
* Insert all the assets inside the assets folder which included images, logo, font-family and icons .ttf/.otf files.
* Used “_” to name the assets except for the font-family and icon .ttf /.otf file as it is when we download it.
* The localization file is directly written in the app folder.

&nbsp;
### 3. Putting imports in an order
1. React import
2. Library imports (Alphabetical order)
3. Absolute imports from the project (Alphabetical order)
4. Relative imports (Alphabetical order)
5. Import * as
6. Import ‘./<some file>.<some extension>

&nbsp;
### 4. Follow the camelCase for the following:
* For the class, variable, function, styling className and etc should be always in camelCase. Avoid using the “_”, “-” or special characters and numbers.

&nbsp;
### 5. Wrapping of the 3rd party libraries in the main component/ top level component.
* To avoid the wrapping of the 3rd party libraries repeated. Please wrap it on the top level components like main.tsx or app.tsx.
> **Best Practice**
  ![5.png](/ui_react/5.png)
> {.is-success}

&nbsp;
### 6. Don’t repeat yourself [DRY]
* One of the basic principles of software development is Don’t Repeat Yourself. We must not write the same piece of code twice. Whenever you write the same piece of code twice, you must try to refactor it into something reusable, even if not completely.
* You can create your own reusable components. 

&nbsp;
### 7.Avoid inline styling
* Try to avoid inline styling as much as possible to have clean code.
* Have the styling files separate.
* Class name should be always in camelCase either you use styled-components or react native styling.

&nbsp;
### 8. Make Sure Your App is Responsive

* You must always make sure that the app you are building is responsive, meaning it is consistent across different devices and platforms.

&nbsp;
### 9.Don’t put logs
* Remove the console log before you push your changes into the release build.

&nbsp;
### 10.CSS unit accept in react-native
* React Native accept are “px” and “%” css units only, avoid using other css units in react native.

&nbsp;
### 11.Implementing styling logically
* When there are two css or more properties to implement logically in the same tag, try to have the style classname and implement it.
* Accepted for the single css property to implement logically in the tag.

&nbsp;
### 12. Line of code for the component should not exceed more than 100. 
* A file should not have more than 100 lines of code.

&nbsp;
### 13. For looping data, make a constant folder and loop data using map function.
* When similar data is repeating, please make a constant folder and loop the data using function such as map. 
> **Best Practice**
  ![13.1.png](/ui_react/13.1.png)
> {.is-success}

&nbsp;
### 14. For theming, all the variables should be defined in ts. Then we will create a global variable in the assets folder.
> **Best Practice**
  ![14.1.png](/ui_react/14.1.png)
  ![14.2.png](/ui_react/14.2.png)
> {.is-success}
  
&nbsp;
### 15. Import of the required library should be particular to a file.
> **Best Practice**
– Use Code reformat
			OR
– github lint
> {.is-success}
  
&nbsp;
### 16. For any logical condition use hook, and interface to pass variable from on component to child component.
* Whenever there is a logical condition, use react hook such as useState, and to pass variables from parent to a child component, use props.

    i) Using use state to show and hide the elements. 
> **Best Practice**
![16.1.1.png](/ui_react/16.1.1.png)
  ![16.1.2.png](/ui_react/16.1.2.png)
> {.is-success}

  ii) Using props and interface to pass data from parent to child.
  > **Best Practice**
  ![16.2.1.png](/ui_react/16.2.1.png)
  ![16.2.2.png](/ui_react/16.2.2.png)
![16.2.3.png](/ui_react/16.2.3.png)
> {.is-success}
 
&nbsp;
### 17. Don’t use {} in className and props unless there are some logical conditions to be written. Value string, don’t use {} (refactor)
Avoid using {} in className unless there are some logical conditions to be written as it makes the code noisy.

> **Best Practice**
 insert img
> {.is-success}
  
> **Bad Practice**
  ![17-bad.png](/ui_react/17-bad.png)
> {.is-danger}

&nbsp;
### 18. React Material 
1. Avoid usage of p, span and div tag. We will use typography, and box layout.
React Material has their own component, that can be modified and used easily in the material configuration (theming)
> **Best Practice**
  ![18.1.png](/ui_react/18.1.png)
> {.is-success}
  
2. We will use mixins that is already provided by Material.
Material provide their own mixin and hence, we don’t have to create our own mixin using  SCSS.

&nbsp; 
### 19. Style Components.

1. Styled Components should be reusable by passing props.
  
Styled Components should be coded in such a way that we can pass probs. This way the styled component can be reused and line of code reduces.
> **Best Practice**
  ![19.1.png](/ui_react/19.1.png)
> {.is-success}
  

2. Component naming should be in Pascal Case. (Prefix should start using Styled)
  
Styled component naming convention should be in Pascal case and should start with ‘Styled’ followed by the component name. This way we can differentiate between normal components and styled component.
> **Best Practice**
  ![19.2.png](/ui_react/19.2.png)
> {.is-success}

3. Common style should in shared.styles.tsx 
> **Best Practice**
![19.3.png](/ui_react/19.3.png)
  > {.is-success}
  
4. UI kits needs to be wrapped by Styled Component (Optional)
  
Kits such as buttons need to be wrapped inside a styled component so that we can pass props to it or easily apply style inside the kits itself.
> **Best Practice**
![19.4.png](/ui_react/19.4.png)
  > {.is-success}
  
# Tailwind
### 1. Make css files
Make a separate file for variable if there are many color variables only, otherwise it can be imported in config file

> **Flies**
 |-application.scss (just imports of files)
	|-component (Classes of only the components of a particular project)
	|-base.scss (tailwind base that you want to change)
	|-variable.scss
	|-form.scss
	|-modal.scss
	|-animations.scss
	|-overwrite.scss
	|-common.scss
> {.is-success}

> <span style="color:#FF0000">If in case separate files are not maintained</span> 
>  <span style="color:#FF0000; font-size: 24px">tw-001: Nu.10</span>
{.is-info}

### 2. Configuration 
Same tailwind configuration to be maintained in all the projects. Make use of JIT.
  
### 3. Make best use of directive in css/scss to make components so as to avoid repetition of long  classes in html.
Ex: @apply, @layer, @variants, etc
Make best use of @apply to make common components such as btn, btn--primary, cards, etc.
More than 6 tailwind class and use case more than two then this to be included in tailwind css component with @apply

> **Flies**
 @layer components { 
    .sk-btn {
      &emsp;@apply h-[40px] rounded-[4px] border cursor-pointer;
        &emsp; &--primary {
          &emsp;	@apply bg-primary text-white;
        &emsp;}
        &emsp; &--secondary {
          &emsp; @apply bg-blue text-white;
        &emsp;}
 		}
> {.is-success}

> <span style="color:#FF0000">If in case separate files are not maintained</span> 
>  <span style="color:#FF0000; font-size: 24px">tw-002: Nu.15</span>
{.is-info}

### 4. Tailwind classes
Make best use of tailwind classes instead of using css porterty

### 5. Let’s not extend colors
Instead of using tailwind colors along with project specific colors, let us only use custom colors. I.e instead of extending colors, specify it outside. 

> <span style="color:#FF0000">If in case extending colors</span> 
>  <span style="color:#FF0000; font-size: 24px">tw-003: Nu.20</span>
{.is-info}

### 6. Root variable - naming convention
Always use colors as variables and variable naming of colors should be similar to the UI convention.
Ex:
primary: 46 204 113; (rgb code can be used so as to generate lighter version)
white: #FFFFFF
black: #000000
  
Not allowed to use bg-[rgba(0,0,0,0.5)], instead derive lighter version of colors from one base color.
  
> **Best Practice**
 	colors: {
        &emsp; primary: withOpacityValue('--primary'),
        &emsp; success: withOpacityValue('--success'),
        &emsp; blue: withOpacityValue('--blue'),
        &emsp; error: withOpacityValue('--error'),
        &emsp; brown: withOpacityValue('--brown')
 	}
> {.is-success}
  
> <span style="color:#FF0000">if found using bg-[rgba(0,0,0,0.5)] to generate lighter color</span> 
>  <span style="color:#FF0000; font-size: 24px">tw-005: Nu.15</span>
{.is-info}

### 7. PX and REM are not to be mixed
Px and Rem units are not to be mixed. All the clases with rem in tailwind should be converted to px. Ex. rounded to rounded-[4px].

> <span style="color:#FF0000">If in case found mixing above mentioned clasess</span> 
>  <span style="color:#FF0000; font-size: 24px">tw-004: Nu.20</span>
{.is-info}

### 8. Gap to be used only with Grid
Gap classes to be used only with grid as there is issue with browser compatibility.

> <span style="color:#FF0000">If in case found using it with flex or others</span> 
>  <span style="color:#FF0000; font-size: 24px">tw-006: Nu.20</span>
{.is-info}

## Hotwire

1. Project prefix for classes
2. Use rails looping for UI repetition
3. Use share directory for common partials if required

### Translations

1. All the translations should be in one level and in case of shared repo use project prefix and all translations in the same level.
Keys to be lowercase and separated by underscores
  eg:   start_shopping: "Start Shopping"

> **Best Practice**
![screen_shot_2022-05-23_at_12.23.33_pm.png](/assets/css/screen_shot_2022-05-23_at_12.23.33_pm.png)
> {.is-success}

2. Avoid conjunctions and prepositions in the key such as a,the, in,an,as.



# Pull Request
#### 1.  Always give a `Proper Branch Name`. Remember to include `UI` at the end of the branch name to differentiate it from `FE branch`.

> **Best Practice**
 feature/event-creation-ui
 feature/profile-ui
 feature/auth-ui
> {.is-success}

> **Bad Practice**
 feature/event-creation-ui-karma
 event_creation
 ft/event-creation
{.is-danger}

> <span style="color:#FF0000; font-size: 24px;">PR-001: Nu. 20</span>
{.is-info}


&nbsp;
#### 2. Make `PR comments` easily comprehensive using these tags along with comments
-for #Mandatory and #Fine the comments have to be resolved immediately
-Reviewers have to make sure not to approve PR unless these two comment tags (#Mandatory and #Fine) are resolved.

> **List of Tags**
 #Doubt
 #Suggestion
 #Refactor
 #Mandatory
 #FutureRecommendation
 #Fine
> {.is-success}

&nbsp;
#### 2. While commiting, the message should be meaningful and understandable. "Commit a command, not a story or gibberish words"
- Never use special characters  for messages.

> **Best Practice**
 git commit -m "layout for student profile "
> {.is-success}

> **Bad Practice**
 git commit -m "layout!" 
{.is-danger}
 
> <span style="color:#FF0000; font-size: 24px;">PR-002: Nu. 30</span>
{.is-info}

- Never use numbers in your message while Commiting

> **Best Practice**
 git commit -m "Responsive Layout"
> {.is-success}

> **Bad Practice**
 git commit -m "Responsive Layout 1"
{.is-danger}

> <span style="color:#FF0000; font-size: 24px;">PR-003: Nu. 30</span>
{.is-info}

&nbsp;
#### 3. Proper title and Description should be given to one's `PR review`.
- From the Title of a PR, the reviewer must get a picture of what the developer has worked on.
- A well described summary of work flow for reviewers to understand.
- Give Proper Tags for the PR.
-  `[WIP]` : If the developer is still working on it.

`Not necessary to tag people if the PR is [WIP].`
- `[NORMAL]` : If it is not required urgently.
- `[RUSH]` : If it is required atleast two days.
- `[URGENT]` : If it is required in same day. (URGENT PR should be merged in the same day if not fine)



`With [RUSH] tag, mention the deadline, and the deadline should be flexible enough for the fellow developers to review pr without intervening their work.(should not be more than two days.)`
- The tag keyword must be prefixed with Project code. e.g [CLUB RUSH]
-  Full Format: `[CLUB RUSH <DD-MM-YYYY>]`
- Example :` [CLUB RUSH 03-12-2022] PR title `



> <span style="color:#FF0000; font-size: 24px;">PR-004: Nu. 20</span>
{.is-info}

&nbsp;
#### 4. Make sure to `Put Screenshots` of UI designs when creating a pull request for your team to review.
- Put the screenshots in the respective component file.
- Put screenshots for any kind of design changes- major or minor.

> <span style="color:#FF0000; font-size: 24px;">PR-005: Nu. 20</span>
{.is-info}

&nbsp;
#### 5.  Always `Include all the UI Team Members` and `FE member(project based)` for your PR review.

> <span style="color:#FF0000; font-size: 24px;">PR-006: Nu. 10</span>
{.is-info}

&nbsp;
#### 6. Always `review PR` that you are tagged in, `before the deadline`.
 
> <span style="color:#FF0000; font-size: 24px;">PR-007: Nu. 30</span>
{.is-info}

&nbsp;
#### 7. Repeating the same mistake or ignoring previous PR comments

> <span style="color:#FF0000; font-size: 24px;">PR-008: Nu. 30</span>
{.is-info}

&nbsp;
#### 8. PR should not be too lengthy.
- Organize PR's in small chunks.

> <span style="color:#FF0000; font-size: 24px;">PR-009: Nu. 20</span>
{.is-info}


# Formatting
#### 1. Formatting does not follow the `convention standard (HTML, SCSS, TS, JSON)`.
![Rule Book](/uploads/rule-book.png "Rule Book")

> <span style="color:#FF0000; font-size: 24px;">FORMAT-001: Nu. 20</span>
{.is-info}

&nbsp;
#### 2. Maximum Lines of code for any SCSS is 500.
> <span style="color:#FF0000; font-size: 24px;">FORMAT-002: Nu. 20</span>
{.is-info}

&nbsp;
#### 3. Always add a Revisit tag when you need to Revisit a code. It can be used in two ways:
***Note***: *Remove this tag after visiting or refactoring your code. Avoid commenting your code in the file or you MUST have a proper title description of why you have done so*.

Formats for revisit tag should be strictly in the following format:
1. REVISIT-TRANSLATE 
	 &nbsp;This tag is used if you need to add the translation later.
2. use TODO as revisit tag
		&nbsp; Eg: TODO BE/FE : comment

> <span style="color:#FF0000; font-size: 24px;">FORMAT-003: Nu. 20</span>
{.is-info}

 &nbsp;
#### 4. Follow a proper format for writing your html code

```html
Syntax:
<div FlexLayoutAttr HTMLAttr 
  [class, type, label, placeholder) 
  [inputData]= “inputData” 
  [outputData]=”outputData” 
  *ngIf="condition" 
  *ngFor="condition" 
  [routerLink]= “link“ 
  (click)= “function“>
</div>

Best Practice																													
Good Code readability 																															 
<mat-select fxLayout="row" fxFlex="100" class="custom-select" *ngIf="condition">									 
  <mat-option value="option" *ngFor="condition">Option</mat-option>	
</mat-select> 											 																														

<sf-input [control]="props('min_price')" 
	[appearance]="'outline'
	[label]="'MINIMUM_PRICE'"
	[type]="'number'"
	[suffixIcon]="'close'
	(clickFunction)="removeValue($event, 'min_price')"  
	[customClass]="'full-width and-cursor'" 
	fxLayout=”row” fxLayout.lg=”column” fxLayout.md=”column-reverse”
	fxLayout.sm=”column-reverse” fxLayout.xs=”column” 
	fxFlex=”20” fxFlex.lg=”100” fxFlex.md=”100” fxFlex.sm=”100” fxFlex.xs=”100”
	fxLayoutAlign=”center center” fxLayoutAlign.lg=”center center” 
	fxLayoutAlign.md=”center center” fxLayoutAlign.sm=”center center” fxLayoutAlign.xs=”center center” 
	class=”hello-world” [class.condition]=”hello-heaven”
	[ngClass]=”{‘hello-paradise’ : condition}” ngClass.md=”hello-hell” ngClass.sm=”hello-hell” ngClass.xs=”hello-hell”
	[inputData]= “inputData”
	[outputData]=”outputData”
	*ngIf="condition"
	*ngFor="condition"
	[routerLink]= “link“
	(click)= “function“>
</sf-input>
```

# Translation

#### 1. One should not miss any translation.
- Always add a comment whether the translation or Data is coming from BE/FE.
```html
Best Practice                                                               #Bad Practise
<span fxFlex="95" class="gray-color">                                       <span fxFlex="95" class="gray-color">
       {{'CANT_RESCHEDULE' | translate }}                                        {{'Can't Reschedule'}}
</span>                                                                     </span>
// REVISIT TRANSLATE																					// Dummy Text, translation from FE
<span> Name </span>																												 <span> Name </span>
```
> <span style="color:#FF0000; font-size: 24px;">TRANS-001: Nu. 20</span>
{.is-info}

&nbsp;
#### 2. One should have a proper name for a translation key. 
- A translation key should always be in uppercase.
- Translation keys should not be too lengthy. Avoid using conjunctions and articles in translation key.
- Do not break your sentence, instead use innerHTML
- For Safire and third party use translation as input and not as attribute.  
- Always use translation prefix depending on the type of your translation.
- Please follow the priority levels of prefix based on which you may use the prefix that you want for the desired translation key
 
&nbsp;&nbsp;&nbsp;1. BTN
&nbsp;&nbsp;&nbsp;2. LABEL
&nbsp;&nbsp;&nbsp;3. HINT
&nbsp;&nbsp;&nbsp;4. QUEST
&nbsp;&nbsp;&nbsp;5. SUCCESS
&nbsp;&nbsp;&nbsp;6. ERROR


- Please add full stop in your `ERROR, SUCCESS and HINT` texts only if  it is a full fledged sentence or long sentence or is a requirement from client/BA.

> **Translation Prefix to be used**
![screen_shot_2021-08-10_at_1.07.59_pm.jpg](/screen_shot_2021-08-10_at_1.07.59_pm.jpg)
 **Best Practice**
 LABEL_NAME
 BTN_ADD
 QUEST_YOUR_NAME
{.is-success}

> **Bad Practice**
 cant_reschedule
 cant_reschedule_your_appointment_for_meeting
 QUEST_WHAT_IS_YOUR_NAME
{.is-danger}

> <span style="color:#FF0000; font-size: 24px;">TRANS-002: Nu. 20</span>
{.is-info}

&nbsp;
#### 3. For a line of long translation that expands beyond one's linting limit, include a backtick and break the line in multiple lines.

> **Best Practice**
 ![screen_shot_2020-06-24_at_5.26.36_pm.png](/ui-conventions/screen_shot_2020-06-24_at_5.26.36_pm.png)
> {.is-success}

> **Bad Practice**
 ![screen_shot_2020-06-24_at_5.26.42_pm.png](/ui-conventions/screen_shot_2020-06-24_at_5.26.42_pm.png)
{.is-danger}

> <span style="color:#FF0000; font-size: 24px;">TRANS-003: Nu. 30</span>
{.is-info}


&nbsp;
#### 4. Proper use of params
- Don't use params when it is at the beginning or end of the sentence.
- param name should be proper.

> **Best Practice**
**en.ts**
'SCHEDULED_RETAILER': 'Scheduled Interaction with Retailer'
 **HTML**
 {{'SCHEDULE_RETAILER' | translate}} {{count}}
> {.is-success}

> **Bad Practice**
**en.ts**
'SCHEDULED_RETAILER': 'Scheduled Interaction with Retailer {{value}}'
**HTML**
 {{'SCHEDULE_RETAILER' | translate : { value: 12 } }}
{.is-danger}

&nbsp;
#### 5. Segregate backend translations in a `folder` or as a separate `file`

> **Best Practice**
**Folder**
Backend
&nbsp; en.json
&nbsp; de.json
**File**
backend_en.json
backend_de.json
> {.is-success}

&nbsp;
#### 6. Do not use abbreviation in translation keys
- The only abbrev allowed is ID or product short keys like NNI.
> **Best Practice**
"LABEL_BASIC_INFORMATION": "Basic Information",
"LABEL_PHONE_NUMBER": "Phone No."
> {.is-success}

> **Bad Practice**
"LABEL_BASIC_INFO": "Basic Information",
"LABEL_PHONE_NO": "Phone No."
{.is-danger}

&nbsp;
#### 7. Avoid adding translations for static text.

> **Bad Practice**
**Examples**:
LABEL_ID
LABEL_SL
LABEL_SELISE
LABEL_HQ etc
{.is-danger}


# Presentation

#### 1. Every two weeks (usually on wednesday) a peer programming team (of two) has to do a presentation on a topic they can select. Teams should be aware of their turn and present on that day accordingly.
> <span style="color:#FF0000; font-size: 24px">PPT-001: Nu. 20</span>
{.is-info}

&nbsp;

 # BEM (Block__Element--Modifier)
 #### The Block, Element, Modifier methodology (commonly referred to as BEM) is a popular naming convention for classes in HTML and CSS. It’s a CSS naming convention for writing cleaner and more readable CSS classes. BEM also aims to write independent CSS blocks in order to reuse them later in your project.

A **BEM** class name includes three parts. 
    1.**Block** - Standalone component that is meaningful on its own.
    2.**Element** - Part of a block that has no standalone meaning.
    3.**Modifier** -  Either a block or element may have a variation signified by a modifier &nbsp; &nbsp;

**BEM class namings**
```html
//Blocks are named as standard CSS classes
.block {
}

//Elements declared with 2 underscores, after block
.block__element {
}

//Modifiers declared with 2 dashes, after block or after element
.block--modifier {
}

//element and modifier together
.block__element--modifier {
}
```

&nbsp;
### 1.Wrongly nested blocks and elements
- It is not allowed to nest blocks. If you start a new block, you are not allowed to proceed with elements from another block.
```html
Bad Practice 																				Best Practice

<div class="card">															   <div class="card">
  <div class="header">															  <div class="card__header">	
    <h2 class="card__headline></h2>									     <h2 class="card__headline></h2>	
  </div>																					     </div>
</div>																					   </div>

```
><span style="color:#FF0000; font-size: 24px">BEM-001: Nu. 20</span>
{.is-info}

&nbsp;
### 2. Great-grandchildren
- There are no grandchildren nor great-grandchildren in BEM. Instead, »normal« elements of the block can be used.
```html
Bad Practice 																				   Best Practice

<div class="card">															        <div class="card">
  <div class="card__header">															  <div class="card__header">	
    <h2 class="card__header__headline></h2>									   <h2 class="card__headline></h2>	
  </div>																					          </div>
</div>																					        </div>

```
><span style="color:#FF0000; font-size: 24px">BEM-002: Nu. 15</span>
{.is-info}

&nbsp;
### 3. Modifiers without a base class
- Modifiers cannot exist without a base block or element.
```html
Bad Practice 																				   Best Practice

<div class="card--highlight">													<div class="card card--highlight">
  <div class="card__header"></div>										  	<div class="card__header"></div>																					         
</div>																					       </div>


Bad Practice 																				   Best Practice

<div class="card">													           <div class="card">
  <div class="card__header--important"></div>							<div class="card__header card__header--important"></div>																					         
</div>																					       </div>

```
><span style="color:#FF0000; font-size: 24px">BEM-003: Nu. 10</span>
{.is-info}

&nbsp;
### 4. Too big blocks
- It is not a good idea to create really big blocks. The idea of BEM is to create modular and reusable blocks.

```html
**Bad Practice**.                                      **Best Practice** 

<body class="body">                                     <body class="body">    
    <header class="body__header"></header>								   <header class="header"></header>	
    <main class="body__main"></main>												 <main class="main"></main>
    <footer class="body__footer"></footer>										<footer class="footer"></footer>
</body>																									 </body>
  ```
 &nbsp;
 
 # Utilities and Suggestions
 ## BEM: button__label--active and button--disabled

- Following are the listed common Utilities we used in the project:
```html
1. Text-align : (text--center, text--left, text--justify and text--right)

2. Cursor : (cursor--pointer, cursor--move, zoom-out, not-allowed and etc)

3. Width : (width--full , width--half)

4. Color : (color--primary, color--secondary, color--black-80 and etc..)

5. Background color : (bg--primary, bg--black-light, and etc..)

6. Font style : (font--normal, font--italic and font--oblique)

7. Font weight : (font--bold, font--lighter and font--normal) 

8. Text-transform : (text--lowercase, text--uppercase and text--capitalize)

9. Display : (display--none, display--inline, display--flex and so on)

10. Position : (position--static, position--absolute, position--fixed and position--sticky)

11. Unset : (unset--all)

12. Border : (border--primary, border--secondary and etc...)

13. Text-decoration : (text--no-decoration, text--overline, text--underline and etc...)

14. Vertical align : (ver--top, ver--baseline, ver--bottom and etc...)

15. White-space : (white-space--nowrap, white-space--pre-wrap, white-space--pre)

16. Float : (float--left and float--right)

17. List-style : (list-style--none)


```
&nbsp;

- For numbers where we use utilities like `margin`,`padding`, `border-radius`,`font-size`,`line-height` and etc

```html
m-2, p-2, fs-12, br-4, mnx-16, lh-16  and etc
```

- Exceptions from mixin
```html
text--truncate,width--full, center--block and etc...
```

# References

1. **CSS Formatting Guidelines**: https://www.drupal.org/docs/develop/standards/css/css-formatting-guidelines
2. **SASS Documentations**: https://sass-lang.com/documentation
3. **SCSS Linting**: https://github.com/brigade/scss-lint
4. **HTML Documentation**: https://devdocs.io/html/
5. **SCSS/SASS/HTML online compiler**: https://www.sassmeister.com/
6. **CSS Guidelines**: https://cssguidelin.es/ 
