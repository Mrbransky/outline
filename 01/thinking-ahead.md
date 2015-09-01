# A taste of the program

A major frustration, forthcoming, will be wrapping your head around the notion of programming. The programming we will be interested in this class will be necessary to cover the parts that HTML and CSS won't be able to do for us, namely:

1. A user does something, and we want that to effect the design or content (events)
2. We want the design or content to do something over, or react to time (animation and timeouts)
3. We don't want the same things to happen in the same way (conditions)

When we create HTML, we are creating **Elements**. An element is also a **Node** (though a node in net necessarily an element). Elements are our building blocks, and right now, they represent content. A paragraph is tucked between \<p\> markup. Now that it is a paragraph, we can make sure it looks a certain way with CSS, and with javascript, we can make it *act* a certain way.

(Make a very quick HTML page, run through some stuff in dev tools.)

## Events, Timeouts, Conditions.

Say we have a box of things - a box of little objects. You're peering down into the box and you have paragraphs, headings, and even boxes filled with other little boxes. But you're main box - the box containing everything - we are going to call it the **Root** box. So, you know there is this paragraph in the root box - there are a bunch of them actually, but you just want the first on you see. You dig around, you **query** the **root** box for it, and you eventually select it. There it is, in your hand. This little paragraph element in your hand, it has a tiny brain in it - but more akin to an alarm clock / parrot. There in your hand, with the paragraph element, you want to be able to tell it do to something - not right away, but to do something later on, to react to something someone else might do. In fact, you want the paraghaph to yell "No Touching!" whenever it feels a poke. You look down into your hand and you tell your paragraph "Listen, when I poke, you yell.". It responds by doing nothing, so you assume it understands otherwise it would complain - it's just a paragraph after all. You test it out... POKE... "Leave me alone!" it says.

<html>
	<body>
		<p>I'm a lil paragraph</p>
	</body>
</html>

var elem = document.querySelector('p');
elem.addEventListener('p', function (evt) {
	alert('No touching!');
}, false);