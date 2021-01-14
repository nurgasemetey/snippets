### flutter general info

> The following assertion was thrown while handling a
> gesture:
> setState() callback argument returned a Future.
> The setState() method on _FooState#236 was called
> with a closure or method that returned a Future.
> Maybe it is marked as "async".
> etc. etc. etc.

Your takeaway is this: when you see one of these, fix the problem. It’s
the right thing to do. But don’t be confused if you don’t see that same
problem after you’ve deployed it.



---



The MaterialApp widget creates the outer framework for your app. As
important as it is, the user never sees the MaterialApp because no parts of it
are technically visible. It wraps your entire app, giving you the opportunity
to give it a title so that when your OS moves the app into the background,
it’ll have a name. This is also where you’ll apply the default theme for your
app – fonts, sizes, colors, and so forth.

---

Whereas the MaterialApp widget creates the outer invisible framework,
the Scaffold widget creates the inner visible framework.

Scaffold has one purpose in life: to lay out the visible structure of your
app to give it the predictable and therefore usable layout that so many
other apps have. It creates, among other things:
• An AppBar for the title
• A section for the body
• A navbar at the bottom or a navigation drawer tothe left
• A floating action button
• A bottom sheet – a section that is usually collapsed but
can be slid up to reveal context-aware information for
the scene that the user is on at that moment

---

You can show a SnackBar in any scene you like as long as you do it in a
widget that is nested inside a Scaffold:

---

In Flutter, every widget on your device’s screen eventually has a
height and a width which it calls the “RenderBox.” Each widget also has
constraints: a minHeight, a minWidth, a maxHeight, and a maxWidth
which it calls the “BoxConstraints.”

---

![img](https://i.imgur.com/AjldWvi.png)

---

Expanded widget
mainAxisAlignment is awesome if the spacing is cut and dried – you want
equal spacing somehow. But what if you don’t want spacing at all? What
if you want the widgets to expand to fill the remaining space? Expanded
widget to the rescue

---

This would not work since Image widgets don’t have a padding,
margin, or borders. But you know what does? Containers!
Web developers often apply these things by wrapping elements in a
generic container called a <div> and then applying styles to create pleasant
spacing for our web pages.

Flutter doesn’t have a `div` , but it does have a div-like widget called
a Container which ... well ... contains other things. In fact, its entire life
purpose is to apply layout and styles to the things inside of it. An HTML
`div` can hold multiple things, but a Flutter Container only holds one
child. It has properties called padding, margin, and decoration.

---

Flutter’s navigation works with stacks. When you want to send the user
to a new scene, you will push() a widget on the top of the stack and the
user sees that widget. Each time you push(), you’re making the stack of
scenes taller and taller. When you are ready for them to go back to where
they were before, you’ll pop() the last scene off the top of the stack, and
what is revealed? The previous scene.

---

Card

[Cards - Material Design](https://material.io/components/cards/flutter#card "Cards - Material Design")



