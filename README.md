
# Pazly Template Developer Guide


# Getting Started

Pazly is a landing page building tool for both non technically skilled users and information technology specialists. It aims to allow users to quickly build high quality, high converting web pages which are completely owned by the users. 

Pazly relies on TailwindCSS and has its own coloring system. If you are a fan of Tailwind CSS and want to help nocoders, freelancers and small businesses make great looking landing pages, this guide is for you. 

Benefits of making templates for Pazly: 

✅ You set your price for your work

✅ You keep all the revenue from your template sales. Pazly does not apply any sales commissions

✅ You get great discounts on Pazly Pro memberships

✅ You help a fast growing number of users who will benefit from your awesome work.


# Github Starter Kit

The easiest way to start is to fork or download the starter kit from Github here https://github.com/pazlydev/template-kit

It contains a simple file with dummy elements and the structure that allows Pazly to read and understand the template.

Download the **index.html** and modify this to your linking


# Color System

Pazly uses its own implementation of the coloring system proposed by the Tailwind CSS team. Since Tailwind uses a plugin system and Pazly targets non technical users, we opted to implement a standalone coloring system which is served through CDN. 

<a href="https://pazly.medium.com/the-pazly-color-system-fdc37ebb02c3" target="_blank"><b>Check the guide on Medium for the class names, rules and color codes.</b></a>


# Template structure

A landing page for Pazly is formed from a set of blocks. Each block has within it editable elements. It is very important to understand the difference between blocks and the elements within the blocks


## Editable Blocks

A block represents a **full width section** of a Pazly webpage. Blocks are relative to their container. Blocks can be moved before or after neighboring blocs. Blocks can be cloned by default. It is a good practice to color blocks one by one. 


## Making Elements Editable

Editable elements should be marked with the `pazly-editable` attribute. This is a set of string values, similar to the `class` attribute and contains identifiers for the editors you want to enable for the selected element. 

Example: 
	<pre>
		<code>
			<button <b>pazly-editable</b>="innerHtml bg href"  class="...
		</code>
	</pre>
**IMPORTANT: Please add these markers at leaf nodes in your HTML tree structure**


### Editing text

Add `innerHtml` to the _pazly-editable_ attribute. This will enable a text editor for the element. Please make sure that the innerHtml contains only text
	<pre>
		<code>
			<a href="" pazly-editable="<b>innerHtml</b> bg href"  class="....
		</code>
	</pre>

### Editing background

Simply add `bg` to the _pazly-editable_ attribute. This will enable the color picker. 

Use the `bg` to enable element level background. Choose this editor for your buttons, links, cards, or areas that you want the user to color differently. 
	<pre>
		<code>
			<a href="" pazly-editable="innerHtml <b>bg</b> href"  class="...
		</code>
	</pre>

**IMPORTANT: The section background picker is assigned out of the box, please do not assign the pazly-editable attribute on the section block.**


### Editing links

Add `href` to the _pazly-editable_ attribute. This will enable the link input editor.  Choose this editor for your buttons and links
	<pre>
		<code>
			<a href="" pazly-editable="innerHtml bg <b>href</b>"  class="....
		</code>
	</pre>

### Editing images

Editing images is as simple as setting the `src` value on the _pazly-editable_ attribute of an image tag. This will enable the image editor which allows you to set an image link or open an image from your computer. The opened image is later transformed into a base64 string. 

**IMPORTANT: Do not use `pazly-editable="src"` on HTML elements that do not support the src attribute natively.**
	<pre>
		<code>
			<img src="" <b>pazly-editable="src"</b>  class="...
		</code>
	</pre>

### Editing videos

Editing video tags is as simple as setting the `src` value on the _pazly-editable_ attribute of a video tag. This will enable the video editor which lets you set a video link. At the moment videos only support one video link, so please use a link that point to a **.mp4 video**

**IMPORTANT: Do not use `pazly-editable="src"` on HTML elements that do not support the src attribute natively.**
	<pre>
		<code>
			<video src="" <b>pazly-editable="src"</b>  class="...
		</code>
	</pre>

### Editing embeddables

To enable embeddables, please construct a wrapper element. Attache the _pazly-editable_ attribute containing the `iframe` value. You can attach other editables like `bg`. 
	<pre>
		<code>
			<div pazly-editable="<b>iframe</b> bg" class="...
				<iframe ...
			</div>
		</code>
	</pre>

### Editing forms

Attache the `form` value to the _pazly-editable_ attribute in the form tag, like in the example below.
	<pre>
		<form pazly-editable=<b>"form"</b> method="POST" action="" static-form="" class="...
	</pre>

# Selling Online (Gumroad, Lemon Squeezy, etc.)
You set your own prices, your own item description. Please add a video demo on how your customers should use the template you make with Pazly Pro. Please also mention they can reach Pazly Pro at https://pazly.dev/


# Getting Featured in Pazly Pro
This means that when Pazly Pro users open the Template panel, your template will show up with a quick link to purchase. This works only with Gumroad for now. 

Instructions on how to submit coming soon...
