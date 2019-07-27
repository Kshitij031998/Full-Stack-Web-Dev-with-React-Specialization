# Components



## Navigation and Navigation Bar

#### Defining Navigation bars

Navbars can be defined as follows:

```
<nav class="navbar bg-primary navbar-dark navbar-expand-sm fixed-top">
	<div class="container">
		...
	</div>
</nav>
```
The container-element can be omitted. If we do not add the container-element, the navbar's content will appear at the top left corner (if no custom styling is applied).

##### Colored Navbars

We can easily can the color theme of our navbar by setting two parameters. The background color can be influenced by means of bg-color classes. In other words, we can choose from `bg-primary`, `bg-success`,  `bg-info`, `.bg-warning`, `bg-danger`, `bg-secondary`, `bg-dark` and `bg-light`.
The font color can be set using the attribute `navbar-dark` (white font color) or `navbar-light` (black font color).

##### Collapsing behavior

We can also control the collapsing behavior of the navigation bar `navbar-expand-{size}` tag. If we set `navbar-expand-sm`, the navbar will spread out vertically for small and extra small screens.

However, it's important to note that the navbar-expand option will NOT display a toggle-button for small screens automatically. It only controls the expansion behavior.

- `navbar-expand` = never collapses vertically (remains horizontal)
- `navbar-expand-sm` = collapses below sm widths <576px
- `navbar-expand-md` = collapses below md widths <768px
- `navbar-expand-lg` = collapses below lg widths <992px
- `navbar-expand-xl` = collapses below xl widths <1200px

##### Fixing the navbar at the top while scrolling

Can be done using the `fixed-top` attribute. It might be required to add additional padding to the websites content to prevent the navbar from overlapping the remaining content.



#### Adding content (logos, links, etc.) to the navigation bar

##### Adding a logo
Adding a logo is easy and can be done using the `navbar-brand` attribute.
```
<nav class="navbar bg-primary navbar-dark navbar-expand-sm fixed-top">
	<div class="container">
		<a class="navbar-brand" href="#">Logo</a>
	</div>
</nav>
```
##### Adding a menu
A full-height and lightweight navigation (including support for dropdowns) can be added using the `navbar-nav` attribute. It's important to note that navigation in navbars will always occupy as much horizontal space as possible to keep its content securely aligned. Therefore, toggler classes need to be used for proper responsive styling.

Active states—with `active`—to indicate the current page can be applied directly to `nav-link`s or their immediate parent `nav-item`s.

```
<nav class="navbar navbar-dark navbar-expand-sm bg-primary">
	<div class="container">
        <ul class="navbar-nav mr-auto">
            <li class="nav-item active"><a class="nav-link" href="#">Home</a></li>
        </ul>
	</div>
</nav>
```

##### Adjusting the menu position

The menu position can be influenced using the `mr-auto` (push items to the left) and `ml-auto` (push items to the right) attribute.

#### Adding a toggle button to collapse the navigation bar

Here's an example of a toggle-button added to the navigation bar. As we can see the button controls the visibility of the component with the id `Navbar`. This requires us to wrap the menu items in a component with the specified id.

```
<nav class="navbar navbar-dark navbar-expand-sm bg-primary">
	<div class="container">
        <button class="navbar-toggler" type="button" data-toggle="collapse" 
         data-target="#Navbar"/>
        </ul>
	</div>
</nav>
```

```
<div class="collapse navbar-collapse" id="Navbar">
	<ul class="navbar-nav mr-auto">
		<li class="nav-item active"><a class="nav-link" href="#">Home</a></li>
		<li class="nav-item"><a class="nav-link" href="./aboutus.html">About</a></li>
     	<li class="nav-item"><a class="nav-link" href="#">Menu</a></li>
   		<li class="nav-item"><a class="nav-link" href="#">Contact</a></li>
	</ul>
</div>
```



## Breadcrumbs

#### What are breadcrumbs?

Secondary navigation which is usually placed below the primary navigation and above the content.

It typically also indicates the current page's location within a navigational hierarchy.

<img src="images/breadcrumbs.png" />



#### Defining breadcrumbs

Breadcrumbs can be defined as follows:

```
<ol class="breadcrumb">
	<li class="breadcrumb-item"><a href="#">Home</a></li>
    <li class="breadcrumb-item active">Library</li>
</ol>
```
