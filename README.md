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









# Pull Request
#### 1.  Always give a `Proper Branch Name`. Remember to include `UI` at the end of the branch name to differentiate it from `FE branch`.
### $${\textcolor{green}{\textsf{----------------------------Best Practice----------------------------}}} {\textcolor{red}{\textsf{----------------------------Bad Practice----------------------------}}}$$
```
 feature/event-creation-ui			feature/event-creation-ui-karma
 feature/profile-ui				event_creation
 feature/auth-ui				ft/event-creation

```
>
> ### $\textcolor{red}{\textsf{PR-001: Nu. 20}}$
>


&nbsp;
#### 2. Make `PR comments` easily comprehensive using these tags along with comments
-for #Mandatory and #Fine the comments have to be resolved immediately
-Reviewers have to make sure not to approve PR unless these two comment tags (#Mandatory and #Fine) are resolved.
### $${\textcolor{green}{\textsf{-------List of Tags----------------------------}}}$$
```
 #Doubt
 #Suggestion
 #Refactor
 #Mandatory
 #FutureRecommendation
 #Fine
```

&nbsp;
#### 2. While commiting, the message should be meaningful and understandable. "Commit a command, not a story or gibberish words"

### $${\textcolor{green}{\textsf{----------------------------Best Practice----------------------------}}} {\textcolor{red}{\textsf{----------------------------Bad Practice----------------------------}}}$$
```
- Never use special characters  for messages.

 	git commit -m "layout for student profile " 				git commit -m “layout!”

- Never use numbers in your message while Commiting

	git commit -m "Responsive Layout" 					git commit -m “Responsive Layout 1”
```

>
> ### $\textcolor{red}{\textsf{PR-003: Nu. 30}}$
>


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
