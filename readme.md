# MarshallBB

This is a variant of my [Marshall](http://github.com/Paladin/Marshall) chess viewer library that is designed to work with backbone.js. It includes a basic model definition for backbone, but feel free to swap that out for a model more appropriate for your use; it's there more as an example than a "must-use" component.

If you roll your own model, the only real requirement of it that it is capable of delivering a simplified JSON equivalent to [PGN](http://www6.chessclub.com/help/PGN-spec). In this case, it wants all the tags from the PGN to be a "tags" structure, and the move text to be in "movetext." (Could I have made it any simpler? Well, I suppose I could have said "put the entire game in a single string variable," but if you have trouble separating the tags from the movetext, take what you need from my basic example model. That's what it's there for, after all.)

There's no ability to save in my example, because Marshall doesn't have game entry capability (yet, he says portentously). If you roll your own model, feel free to make your data entry however you like. Feel free to show it to me; maybe I can use it in a future version. If I were to build one for the demo, it'd be a simple textarea you paste the PGN game data into and submit.

## Then what is it?

Basically, it's a view. You store/retrieve your chess data however you like, then pass it into this to interact with it. The included demo shows it working in context with a page holding other content as well, so you can see how you might use it in conjunction with a general chess website.

Because it's backbone, I'll have some other components involved, but the main "juice" of this is in the view and the library objects it uses.

## Why backbone.js?

Because I wanted to.

## Then Where Is It?

I didn't include [backbone.js](http://github.com/documentcloud/backbone) in this repo for two reasons. First, it's not my code, and second, this should work with all future versions of backbone, and if I included backbone here, then I'd have to update this repo every time backbone updated. I'm lazy; I'd prefer to update this repo only when I have something to add to or fix in Marshall. Go download it yourself; it's not hard. Trust me on this.

Besides, if you want to run the demo or the tests, you'll *have* to download and install it. Look in the demo or  testrunner files to see where you should put it. And if you want to see a demo *before* you download backbone, check the original [Marshall](http://github.com/Paladin/Marshall) repo. It's the same code at the heart of it.