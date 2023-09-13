Let's build the 'I Am Rich' app. Rationale: someone built an 'I Am Rich' app for $999 that just displayed a red ruby on the screen, and it got bought a couple times. They did get banned from the App Store, so let's not do that part.

Storyboards are an option while creating an XCode project in the menu.
## Setup

iOS is the most flexible project setup option and assumes less about your project.

The bundle identifier in the config is like a reverse domain name, getting more and more specific to identify your app as yours with a unique ID.
### _Getting Comfortable With XCode

In the General tab of the project config, which you can get to by going into the file view and clicking on the top level element, you can change the version, identifier, _target iOS version_, _device orientation_, and _status bar_.

XCode is usually split into a couple parts, diagrammed below.

	Aside: the top status bar is similar to the iTunes one. c:

Note that there are tabs on the Navigation and Inspector pane, so if they look different, that's probably why.

For Storyboard view (`.storyboard` files):
	1. there's a `+` button in the top right to add things
	2. the sizing tab is very helpful
	3. the Document Outline is helpful for selecting things between layers

Most pieces can be shown / hidden as apt.

![[Pasted image 20230912200325.png]]

You might find the following helpful when putting things into Anki:

![[Pasted image 20230912210753.png]]

Use Cmd-Minus and Cmd-Plus to change the font.
## Design

The `LaunchScreen.storyboard` is what you can use to edit what shows up while your app is loading.

Storyboard has a couple features:

* You can change the phone canvas, dark / light, and orientation on a storyboard with the bottom buttons.
* You can pan around in your canvas.
* Set the background in the view. Set view settings in the view outline.

Design:

* iOS phones have a fixed virtual width.
* You can drag in your assets in directly. There will be a 1x, 2x, and 3x version, which is meant to accommodate different image sizes. The easiest way to do this is by creating the 3x version first. (ex. 300x300 => 200x200 => 100x100).
* In your Assets folder, you have AppIcon, which shows all the slots that you need to provide, ex. for notifications, various places in the app, various devices, etc.

Design tools:

* You can pick colors from `colorhunt.co`.
* You can create app icons and general images using `appicon.co`.
	* With this site, it puts images in the right format for XCode to put things in the right slots.
* To make icon images themselves, you can go to `canva.com`.

### Running

You can change the simulator it runs in in the top bar.

Running on your physical device:
1. you need to make sure that your XCode and iOS align. Settings -> General -> About on iPhone, and then check XCode -> About.
### Succeeding

Something that helps is having goals, and telling yourself about why you have those goals and why you want to do them. You should have them visible while you work.
## Tasks

- [x] commit current changes
- [x] bump SSH version
- [x] add burger icon
- [x] commit those
- [x] fix warnings / errors
- [x] push em to your GitHub
- [x] clean up your notes
- [ ] push those
- [ ] Anki everything
- [ ] do some long term planning
- [ ] add a README photo and a quick explanation
- [ ] add brag sheet
- [ ] maybe write a blog post about it? and push that
