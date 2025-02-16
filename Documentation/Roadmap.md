# Vision, Technical Considerations and Roadmap

## Vision
IBAnimatable is an Open Source library to help designers and developers design and prototype UI, interaction, navigation, transition and animation for App Store ready Apps in Interface Builder.

## Approaches
* Adding convenient `@IBInspectable` properties to reduce numerous amount of manual code. e.g.`fillColor`, `cornerRadius`, `shadowColor` and `shadowOffset`.
* Providing predefined UI elements and animations. e.g. Flat UI colors, Gradient colors and pop animation.
* Extending existing behaviours, e.g. More transition animations than "Cover Vertical", "Flip Horizontal" and "Cross Dissolve".


## Technical Considerations
* **UIKit** - All `IBAnimatable` UI elements are based on UIkit.
 	* **Dos**
		* All UI elements should support Auto Layout.
	* **Don'ts**
		* Creating another layout system. e.g. flexbox.
		* Creating custom navigation pattern. 
	
* **`@IBDesginable` and `@IBInspectable`** - To design in Interface Builder, all properties should be `@IBDesginable`. Some properties cannot render properly in Interface Builder, e.g. `rotate`. And animations are not able to previewed in Interface Builder. But once Interface Builder supports, those features will work properly in Interface Builder.

* **Platform - iOS** - Currently, `IBAnimatable` focus on iOS only. Once iOS support is mature, we can implement more protocol extensions to support other platforms like MacOS, WatchOS and tvOS.

	
* **iOS version** - Currently, `IBAnimatable` supports iOS 8 and above. 
    * **Dos**
		* Supporting latest version first and disabling them in previous version if required.
	* **Don'ts**
		* Sacrificing features for backward compatibilities.

* **Swift** - Currently, `IBAnimatable` supports Swift only. 
	* **Dos**
		* Using Swift features and best practice like protocol extensions and optional.
	* **Don'ts**
		* Avoiding Swift features to support Objective C.

## Roadmap
### Designable elements
* Bar Button Item: 
	* <del>roundedImage</del> 
	
* Blur: 
	* <del>blurEffectStyle</del>
	* <del>blurOpacity</del>
	* Motion Blur
	
* Border: 
	* <del>borderColor</del>
	* <del>borderWidth</del>
	* <del>borderSide</del>
	* Border with more than one side and less than 4 sides
	
* Check Box: 
	* <del>checked</del>
	* <del>checkedImage</del>
	* <del>uncheckedImage</del>
	* Animations for state changes
	* Default checked and unchecked icon (path to avoid image assets?)
	* Checked color
	
* Corner: 
	* <del>cornerRadius</del>	
	
* Fill: 
	* <del>fillColor</del>
	* <del>opacity</del>
	
* Gradient: 
	* <del>startColor</del>
	* <del>endColor</del>
	* <del>startPoint</del>
	* Default gradient colors
	
* Navigation Bar: 
	* <del>solidColor</del>
	
* Mask: 
	* <del>Circle</del>
	* <del>Star</del>
	* Polygon
	* Triangle
	
* Padding: 
	* <del>paddingLeft</del>
	* <del>paddingRight</del>
	* <del>paddingSide</del>
	
* Placeholder: 
	* <del>placeholderColor</del>
	
* Root Window: 
	* <del>rootWindowBackgroundColor</del>
	
* Rotation: 
	* <del>rotate</del>
	
* Shadow: 
	* <del>shadowColor</del>
	* <del>shadowRadius</del>
	* <del>shadowOpacity</del>
	* <del>shadowOffset</del>
	
* SideImage: 
	* <del>leftImage</del>
	* <del>leftImageLeftPadding</del>
	* <del>leftImageRightPadding</del>
	* <del>leftImageTopPadding</del>
	* rightImage?
	* RightImageLeftPadding?
	* RightImageRightPadding?
	* RightImageTopPadding?
	
* Status Bar: 
	* <del>lightStatusBar</del>
	
* Table View Cell: 
	* <del>removeSeparatorMargins</del>
	
* Tint: 
	* <del>tintOpacity</del>
	* <del>shadeOpacity</del>
	* <del>toneColor</del>
	* <del>toneOpacity</del>
	
* View Controller: 
	* <del>hideNavigationBar</del>

* Collection View and Collection View Cell
* Slider
* Material Design elements	
* Flat colors
* Motion effect, parallax effect

### Animatable elements
* Animations types:
	* <del>SlideInLeft</del>
	* <del>SlideInRight</del>
	* <del>SlideInDown</del>
	* <del>SlideInUp</del>
	* <del>SlideOutLeft</del>
	* <del>SlideOutRight</del>
	* <del>SlideOutDown</del>
	* <del>SlideOutUp</del>
	* <del>SqueezeInLeft</del>
	* <del>SqueezeInRight</del>
	* <del>SqueezeInDown</del>
	* <del>SqueezeInUp</del>
	* <del>SqueezeOutLeft</del>
	* <del>SqueezeOutRight</del>
	* <del>SqueezeOutDown</del>
	* <del>SqueezeOutUp</del>
	* <del>FadeIn</del>
	* <del>FadeOut</del>
	* <del>FadeOutIn</del>
	* <del>FadeInOut</del>
	* <del>FadeInLeft</del>
	* <del>FadeInRight</del>
	* <del>FadeInDown</del>
	* <del>FadeInUp</del>
	* <del>FadeOutLeft</del>
	* <del>FadeOutRight</del>
	* <del>FadeOutDown</del>
	* <del>FadeOutUp</del>
	* <del>SqueezeFadeInLeft</del>
	* <del>SqueezeFadeInRight</del>
	* <del>SqueezeFadeInDown</del>
	* <del>SqueezeFadeInUp</del>
	* <del>SqueezeFadeOutLeft</del>
	* <del>SqueezeFadeOutRight</del>
	* <del>SqueezeFadeOutDown</del>
	* <del>SqueezeFadeOutUp</del>
	* <del>ZoomIn</del>
	* <del>ZoomOut</del>
	* <del>Shake</del>
	* <del>Pop</del>
	* <del>FlipX</del>
	* <del>FlipY</del>
	* <del>Morph</del>
	* <del>Squeeze</del>
	* <del>Flash</del>
	* <del>Wobble</del>
	* <del>Swing</del>
	* <del>Rotate</del>
	* MoveX
	* MoveY
	* MoveXY
	* Jump
	
* Animation properties: 
	* <del>animationType</del>
	* <del>autoRun</del>
	* <del>duration</del>
	* <del>delay</del>
	* <del>damping</del>
	* <del>velocity</del>
	* <del>force</del>
	* <del>repeatCount</del>
	* Animating forever? `repeatCount = Float.Infinit`
	* timing: linear and easing
	
### Interaction elements
* AnimatablePopupController: 
	* gestureToDismiss (UIDynamics)
	
* AnimatableAlert​Controller or DesignableAlert​Controller: - `UIAlert​Controller`
	* Standard Alert
	* Action Sheet
	
* Ripple effect for taps

* Dismissing keyboard automatically when tap outside of the `AnimatableTextField`

* Automatically scrolling the view to follow the keyboard's focus.
 	
### Navigation and transitioning animators
* Navigation animators to replace `navigationController.delage`. e.g. swip-up to pushViewController
* Meaningful transition like https://www.google.com/design/spec/animation/meaningful-transitions.html
* More transition like https://github.com/ColinEberhardt/VCTransitionsLibrary and http://transitiontreasury.com/
* 

### Misc.
* Importing Sketch to Swift playground
* Importing Sketch to Storyboard? Maybe too hard.
* Sketch plugin to export `IBAnimatable` styles from Sketch, e.g. generating `Opacity=0.5; fillColor=#336699;` from Sketch and easily apply in Interface Builder.

**Any suggestions toward to the vision are welcome**, please modify the Roadmap.md file and create PR.
