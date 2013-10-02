# HTML
So, you want to make websites? You've come to the right place! The first stop on your way to being a web developer is HTML.

## What is HTML?
First things first: HTML is not a programming language. It's what's known as a 'markup language.' That means it is used to describe how things are structured, not how they function. HTML actually stands for 'Hyper-Text Markup Language.' 

HTML is the first part of what we'll call the 'Web Trifecta.' The Web Trifecta is made up of:

1. **HTML**: The semantics of the site.
2. **CSS**: The presentation of the site.
3. **JavaScript**: The behavior of the site.

The real purpose of HTML is to dictate the *semantics* of the site, or what everything represents. For instace, do you have some paragraphs of text? Or a heading? Or a list of items? HTML describes the meaning and purpose of these items.

HTML accomplishes this by using *tags*. What's a tag? Well, it looks something like this:

```
<p>With great power, comes great responsibility.</p>
```

The ```<p>``` thing is what's known as a paragraph tag, and it says that everything inside it represents a paragraph of text. The tag is terminated by a tag has the same name, but has a ```/``` in front. In this case, the terminating tag is ```</p>```. So, this says we have a paragraph with the contents ```With great power, comes great responsibility.```

There are lots of tags, and HTML is basically just a collection of them. Most of this guide will be describing a bunch of tags and enforcing good style when writing HTML.

## A General HTML Template
When it comes to making a website, you always want to start with a template similar to this:

```HTML
<!DOCTYPE html>
<html>
  <head>
    <title>Peter Parker</title>
  </head>
  <body>
    <p>Welcome to my WEB site.</p>
  </body>
</html>
```

So, the first thing you'll notice is that there's lots of tags, and there's tags within tags. We'll go through each fo the tags, so no need to worry about that. As far as the nested tags are concerned, it's easy to follow just by looking at where each tag starts and ends. Most people use indentation to indicate where a tag starts and ends as well (and you should too!) so that makes it even easier.

So, let's go through each tag.

* ```<!DOCTYPE html>```: This tells the browser that you're going to be giving it HTML content. You'll find that most websites will work just fine without this, but occasionally omitting it will break some things, so be sure to always include it.
* ```<html></html>```: Indicates the start and end of the HTML content. Everything goes inside this tag.
* ```<head></head>```: Contains the header info of the site. This isn't visible to the user. You can specify the title here. When we get to CSS, we'll be linking in stylesheets here. 
* ```<title></title>```: The title of the page. This is the text that shows up on the tab label.
* ```<body></body>```: All visible content of the site goes in the body of the page.
* ```<p></p>```: A paragraph of text.

## Poppin' Tags
HTML is all about tags, so let's just run through a bunch.

### Emphasis!
There are two tags that provide different kinds of emphasis in HTML: ```<strong>``` and ```<em>```. 

```HTML
<p>
  This is my <strong>gift</strong>; My <em>curse</em>. Who am I?
</p>
<p>
  I'm <strong><em>Spider-Man</em></strong>.
</p>
```

Now, the default way the browser renders the ```<strong>``` tag is to make the text bold, and the default way it renders the ```<em>``` tag is to make the text italic. However, that's not the point of HTML. Always remember that HTML defines semantics, **not** appearance. Using CSS, we can make the ```<em>``` tag look however we want. When writing the HTML, we are just indicating that the text has emphasis - **not** how that emphasis is conveyed visually.

### Headings!
Headings in HTML are just like headings in Word or Google Docs: They give titles to sections of content. Here are some examples:

```HTML
<h1>The most important section!</h1>
<h2>Almost the most important!</h2>
<h3>This section is pretty cool.</h3>
<h4>Eh, you could skip over me.</h4>
<h5>I'm not useful at all.</h5>
<h6>Why am I even here?</h6>
```

Here, you can see that heading tags range from ```<h1>``` to ```<h6>```, with ```<h1>``` being the most important. Notice I say 'most important' and not 'biggest' or 'boldest.' Remember, HTML conveys the semantics and structure of a page, not its appearance. We can make headings look however we want with CSS when we get there.

### Lists!
A list is just a group of related items. There's two types: ordered, and unorderd. In ordered lists, the order of the items matters. Here's an example of an ordered list:

```HTML
<h1>How to Become Spider-Man</h1>
<ol>
  <li>Go on a school fieldtrip.</li>
  <li>Get bit by a radioactive spider.</li>
  <li>Have a life-altering event that shows you the importance of using your powers for the benefit of others.</li>
  <li>Become Spider-Man.</li>
</ol>
```

So there's two new tags here, ```<ol>``` and ```<li>```. The ```<ol>``` tag indicates that it's an ordered list. The ```<li>``` indicates an item in that list. Simple right? Now what if we wanted to do an unorderd list, where the order of our items doesn't matter? We just have to replace the ```<ol>``` tag with an ```<ul>``` tag, like so:

```HTML
<h1>The Sinister Six</h1>
<ul>
  <li>Doctor Octopus</li>
  <li>Vulture</li>
  <li>Electro</li>
  <li>Shocker</li>
  <li>Mysterio</li>
  <li>Kraven</li>
</ul>
```

### Links!
Ah yes, those little blue links, how could we ever forget those? Links let you move between web pages. Here's an example of a link that will take you to an awesome web page.

```HTML
<a href="http://en.wikipedia.org/wiki/Spider-Man">Click Me!</a>
```

So, we've learned two things here: one, the link tag is ```<a>``` (which stands for 'anchor'), and two, apparently you can put other stuff in the tag too. In this case, we have a property called ```href``` in there. ```href``` tells us what the link points to. In this case, it points to the best Wikipedia page ever written.

### Images!
Everybody loves pictures. Good thing there's a tag for that!

```HTML
<img src="img/pic.jpg" />
```

The big thing here is that ```src``` attribute. This just contains a relative path to the image that you want to display. We recommend that you keep all of your pictures in a folder called ```img``` or ```images```, as it keeps things organized.

### Tables!
Do you have tabular data that you want to display in a grid? Then you want a table! Tables have three main tags: ```<table>```, ```<tr>```, ```<td>```, and ```<th>```. Take a look at this example, and then we'll explain afterwards.

```HTML
<table>
  <tr>
    <th>Villian</th>
    <th>Has Spider-Man Beat Them?</th>
  </tr>
  <tr>
    <td>Venom</td>
    <td>Yes</td>
  </tr>
  <tr>
    <td>Doctor Octopus</td>
    <td>Yes</td>
  </tr>
  <tr>
    <td>Sandman</td>
    <td>Yes</td>
  </tr>
</table>
```

This will make a table with the column headings 'Villian' and 'Has Spider-Man Beat Them?' Then, each row will be "Venom | Yes", "Doctor Octopus | Yes", and "Sandman | Yes". Given that info, can you guess what the tags mean? 

```<tr>``` is table row, as it defines a row in the table. ```<th>``` is a table heading, and ```<td>``` is a table data cell. 

Tables have gotten a lot of hate in the web development community over the past few years. That's because they were being heavily misused. Developers were creating entire sites using tables because it was easy to do the layout like that. However, going back to our Web Trifecta, you know that's not a good idea. HTLM defines the semantics of sites, not the appearance. Therefore, tables should only be used for tabular data - NOT for general site layout.

### Generic Blocks of Text!
There may be a point when you realize that you have text whose semantics can't be properly captured with an existing tag. In this case, you can use the ```<div>``` tag or the ```<span>``` tag.

```HTML
<div>I'm pretty generic.</div>
<span>Yeah, me too.</span>
```

You may wonder why you would use a generic tag like this, and what the differences are between ```<div>``` and ```<span>```. Don't worry, all will be made clear in our CSS guide. 

### Form Elements!
Need to have the user input data? Forms are the answer. There's lots of form elements, and here we'll just cover the most popular.

#### Text Fields
Text fields are just those little one-line text boxes that people can type stuff into.

```HTML
<input type="text" />
```
Notice how there's no closing tag? That's because some tages, like the input tag, don't need a closing tag. You just close it *inside* the tag, hence the ```/``` at the end there.

#### Text Areas
A text area is that big block of text people can enter multi-line input into.
```HTML
<textarea>Default Text</textarea>
```
If you want some text to show up by default, just put it inside the tag.

#### Buttons
Want to have a button? Here's how!
```HTML
<input type="button" value="Click Me!" />
```
And there's you're button! The ```value``` property dictates what the button text will be.

# What Should I Use to Write Code?
People are pretty passionate about what code editor they like to use. We'll list a couple of options here, both free and paid, and we'll leave itup to you to try them out and decide (but let's just say you should probably use Sublime). 

## Sublime Text 2
Sublime is probably the coolest/hippest code editor out there right now, and that's one of its biggest advantages. It has a great community and therefore TONS of plugins. Some great default features are multiple cursors, tons of syntax highlighting options, awesome snippet support, and a super-userful built-in build system creator. To manage all of these plugins, you'll definitely want to install the package manager listed below.

On top of all of this, Sublime is probably the fastet

**Cost**: Sublime technically requires a license, but you can consider it nagware. It has an unlimited free trial where it'll ask you to buy it every 10 saves or so. You can just ignore it. However, if you like it, of course buy a license. Developers gotta eat.

**Links**
* [Download](http://www.sublimetext.com/2)
* [Package Manager](https://sublime.wbond.net/installation#st2)
* [Fantastic Tutorial Series](https://tutsplus.com/course/improve-workflow-in-sublime-text-2/#tips,_techniques_and_modifications)

## WebStorm/PHPStorm
Whereas Sublime is a relatively bare-bones text editort that relies on plugins to give it most of its functionality, WebStorm is a full-blown IDE that is jam-packed with features from the get-go. It probably has the best code-completion of all the web IDE's, including some really great support for things like TypeScript and CoffeeScript. Don't underestimate the power of a good auto-complete. If you get PHPStorm (which is the same as WebStorm + PHP), then you'll get fantastic PHP support as well.

And hey, it's made by the same people that make IntelliJ (arguably the best Java IDE), so you know it's going to be stable and have great developer support.

**Cost**: $49 ($29 for academic license)

**Links**
* [Download](http://www.jetbrains.com/webstorm/)
