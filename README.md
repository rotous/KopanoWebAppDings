# KopanoWebAppDings
A free font that can be used to display the WingDings smilies that Outlook creates.

## Introduction
At Kopano we had an issue with HTML mails that were sent with Microsoft Outlook and that contained smilies. When a user types an ascii smilie, e.g. :), Outlook will convert this to a WingDings smilie, e.g. &lt;span style="font-family:Wingdings"&gt;J&lt;/span&gt;. Needless to say that any user that was using our mail client Kopano WebApp and didn't have the Wingdings font installed (or if it was installed and the user was using FireFox which blocks symbol fonts) just saw a strange J in the message. To fix the problem we decided to create our own font that we can use to display smilies without changing the original message.

## Usage
To use the font on webpages copy the fonts directory to your server and add the following lines to your CSS.

    @font-face {
    	font-family: 'Wingdings';
    	src: url('<RELATIVE_PATH_TO_FONTS>/kopanowebappdings.eot');
    	src: url('<RELATIVE_PATH_TO_FONTS>/kopanowebappdings.eot?#iefix') format('embedded-opentype'),
    		url('<RELATIVE_PATH_TO_FONTS>/kopanowebappdings.woff2') format('woff2'),
    		url('<RELATIVE_PATH_TO_FONTS>/kopanowebappdings.woff') format('woff'),
    		url('<RELATIVE_PATH_TO_FONTS>/kopanowebappdings.ttf') format('truetype');
    	font-weight: normal;
    	font-style: normal;
    }
    
The smilies should now be visible.

_Note: The Wingdings font contains much more characters than just the three smilies in our font. We chose not to create replacements for the other character because they never caused issues for us, but you should be aware of the fact that this is not a full replacement font!_

## Special thanks
Special thanks go out to WebDesigner Depot, that created a great tutorial on how to create an icon font: http://www.webdesignerdepot.com/2012/01/how-to-make-your-own-icon-webfont/

We also thank the Inkscape team for creating an awesome piece of (free!) software that we used to create our font: https://inkscape.org/

And last but not least we would like to thank Transfonter for creating the different font types: http://transfonter.org/
