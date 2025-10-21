# javascript-DOM-practice-1

I would like to use DOM to make some changes to the HTML:
I would like to add a class .huge and in DOM make the h1 .huge size. 
I inserted this code in console: document.querySelector("h1").classList.add("huge");
but this was the error: unidentified


=====

Hey Lindsey, good news!  The code that you are pasting into the console is actually working... 
1. Reload and try running this again: document.querySelector("h1").classList.add("huge");
2. Then right click on the red 'Hello' at the top of the page and select 'inspect'...  That will open the DOM inspector.  You should see something that looks like this:
<h1 class="huge">Hello</h1>

The class "huge" wasn't there before, which means that Javascript added it dynamically, so your code is working!  The 'undefined' that you are seeing isn't an error...  When you do something like .querySelector, .add, etc, you are calling 'methods' on javascript 'objects'.  All methods return something...  It could be a string, or a number, or sometimes it's 'nothing', which is why you are seeing 'undefined' (because those methods don't return anything.)

You can style the h1 tag in your style.css file.  Try adding something like this:

h1.huge {
  font-size: 50px;
}

When you see a website, you are seeing the visual representation of the DOM.  The DOM is the underlying structure of the HTML...  Sort of like the boards that make a house.  You see the walls, but underneath the walls are the boards, which is what the DOM is to a website.  When you right click on something and 'inspect', you are looking at the DOM in the inspector.  Javascript is used primarily to make dynamic changes to the DOM.