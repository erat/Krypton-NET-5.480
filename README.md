# <img src="https://github.com/Wagnerp/Krypton-NET-4.72/blob/master/Assets/PNG/Square%20Design/Main%20Icon/64%20x%2064/Square%20Design%2064%20x%2064%20New%20Green.png">-NET-4.80

=======

# ["Toolkit help index"](https://rawgit.com/Wagnerp/Krypton-NET-4.7/master/Help/Output/index.html)

=======

## NOTE: With the advent of Windows 10 1803 being released to the general public, I am pleased to announce the availability of a 4.72 release that will support the .NET 4.7.2 framework. You can follow the project [here](https://github.com/Wagnerp/Krypton-NET-4.72). 

## WARNING: If you are **NOT** using Windows 10 Aniversary update or higher **or** Windows Server 2016 or higher, then this will not work for you. Also, this is using a alpha/beta version of a .NET framework, so it is not production ready!

=======

## 2018-09-25 Build 643
* Allow the developer to override the `Ctrl+c to copy` text in the Caption
* The `Import()` and `Export()` methods will now use the native `KryptonMessageBox` instead of a system one
* Removed the phantom `KryptonPalette` component
* Now you can access the full `FilePath` of the loaded palette XML file
* New icon (not propagated through all the example applications yet)
* Fix KryptonForm does not respect Minimum Size set in designer #57
  * And sort out some spelling mistakes in the `VisualForm.cs`
* `SeparatorController.cs` & `DragObject` bug fix, #79
  * Fix for bug Issue, #79, courtesy of [James Simms](https://github.com/jwsimms)
* General bugfixes

=======

## 2018-06-14 Initial Commit

* Uploaded build 3621 of .Net framework 4.8 for easier access.
* Fixed references that blocked demo applications from launching.
* Start work on getting the system themes to display the extras. 
  * Not perfect but at least the "Chrome" displays the intended buttons and text(s).
* Removal of "not needed" casts.
* Remove the Designer dll (Project / code moved in Git)
* Place designers into actual dlls (Small size increase)
* Fix fallout from Designer dll removal from other projects
  * Fix build path output, and Demo Apps Ref path import and Output
* Remove hard-coded directory offsets for Component outputs
* Use offset location for components in Demo Apps 
* Remove Release GAC'ing
* Fix explorer for the copied target names
* DLL assembly names have been renamed to `Krypton Design`, `Krypton Docking`, `Krypton Navigator`, `Krypton Ribbon`, `Krypton Toolkit` and `Krypton Workspace`, these changes do also apply to other binaries in this repo. However these changes does **NOT** affect the namespace names of `ComponentFactory.Krypton.xx`.
* Build output paths have been changed for easier installer authouring and syncronisation.
* Removed different architectures folder for easier navigation.
* All binaries, applications, tools etc in this project will now be installed by one installer, powered by Advanced Installer. This is to allow easier distribution, and easier end-user updating.
* New folder `Updates` to contain files needed for the new update distribution.
* Don't forget to add the TextExtra into the title width calculation
* Only Display "Ctrl+C..." for Error and Exclamation icon's
* Change the projects to at least recognise C#7.2 features and enhancements - _to be applied in the future_
* Some tinkering with spelling corrections - _to be applied in the future_
* Make the Help relevant to the Actual Code #17
* Change `bmp`'s to `png`'s
* Fix location of source for Help
* Change output to be clearer
* Remove previous output *leftovers*
* Add instructions on how to generate
* MessageBox taking a Null window owner (via default API's / null start / No KryptonManager loaded)
* Sort out the Toolkit examples to use the new dll locations
* Remove `BootstrapperPackage` .Net 3.5 nonsense from projects
* Remove hard coded build `Output Paths`
* The palette upgrade tool is now back! Enhancements over previous commercial version 4.4.0 include:
- Ability to export upgraded palette XML files
- Check to see if the output palette file is not saved before closing
* Exploration into a console version is in the works
* Changed some classes from `internal` to `public` for easier accessibility for the **Extended Toolkit**
* All AMD64/x64 solutions should now build into correct directories
* Renamed everything labeled `2015` to `2018`
* Palette designer has been included with this release and future releases.
* Added descriptions to 'OnTrackMouseEnter' and 'OnTrackMouseLeave' events to make more sense
* Renamed 'GetCreateParams()' method to 'DrawDropShadow()' in 'KryptonForm.cs' to avoid confusion
* Added/update documentation/comments for drop shadow methods in 'KryptonForm.cs' to make functions clearer
* Convert to `'?:` expression
  * `null-coalescing` if applicable
  * Then to `Expression body` if simplified enough
* Fix some spelling mistakes along the way
* Add Ctrl+c text to `KryptonCommand`
* Fixed bug [Screen artifact, #79](https://github.com/ComponentFactory/Krypton/issues/79) courtesy of Cocotteseb
* Attempt at including drop shadow around the form
* Begin work on fixing bug [Screen artifact, #79](https://github.com/ComponentFactory/Krypton/issues/79)
* Groundwork for Visual Studio project & item templates
* Fix `AssemblyCopyright` information date ranges
* Create a Test project demonstrating MessageBox usage
  * Fix Mangled Caption that may contain carriage returns
  * Fix Box clipping on long and short text combinations
  * Add Extra text showing that Ctrl+C works in a `KryptonMessageBox`
* Code Headers changed:
  * Add correct license term and date range for ComponentFactory
  * Moved Wagnerp and Smurf-IV to later
* Use `nameof` for exception parameter references
* Add /// comments (on some public API's) stating that an exception can be returned if it explicitly __throws new__
* To reflect the .Net version move to Major.Minor of 4.80
* Build will increment, with the final useless installable number left at zero
* Use "[Automatic Versions](https://marketplace.visualstudio.com/items?itemName=PrecisionInfinity.AutomaticVersions)" to perform the update build number action
* Message content size adjustment in KryptonTaskDialog; ComponentFactory commit [5463f83](https://github.com/ComponentFactory/Krypton/commit/5463f835bcdbfffbafc9002923e0bea831bed211)
* Remove "Assignment is not used"
* Initialise orientation in mementos correctly
* CherryPick Merges from Cocotteseb 
  * Docking : Get the KryptonWorkspaceCell from a page; commit [ea42f5f](https://github.com/Cocotteseb/Krypton/commit/fe2e778d49216215b8fb51c03c9ac3170f5a67c3)
  * Improvements to Krypton Workspace; commit [fe2e778](https://github.com/Cocotteseb/Krypton/commit/fe2e778d49216215b8fb51c03c9ac3170f5a67c3)
  * Draw text without a glowing background, for use on a composition element; commit [0286bd1](https://github.com/Cocotteseb/Krypton/commit/d3876704ad0ec24f5379a7febc1e3c3a1844e8af)
  * Modifications required for Krypton OutlookGrid; commit [d387670](https://github.com/Cocotteseb/Krypton/commit/7adde64817cfaa3967da1773774949a37d4b4a84)
  * Fixed an exception crash in KryptonTreeView; commit [7adde64](https://github.com/Cocotteseb/Krypton/commit/8d529d7a624c71c3ce22a7205f9116f0d443bb64)
  * Improvements Office2010 Black and first try Render Office 2013; commit [8d529d7](https://github.com/Cocotteseb/Krypton/commit/f85b69403a2e4359c546fb7d959dfd2c737491f1)
  * Windows 10 1511 enhancements + maximized windows bug fix trying; commit [71e5f32](https://github.com/Cocotteseb/Krypton/commit/621ab7c5ca1d7cd47f2c527ae1c18731b622b846)
  * Added KryptonMenuImageSelect click event; commit [621ab7c](https://github.com/Cocotteseb/Krypton/commit/ef4a415b84ac4ce9b145db9d723701a0099ce0f1)
  * Trying to fixed rare crashed in KryptonRibbon Composition; commit [ef4a415](https://github.com/Cocotteseb/Krypton/commit/c55aeadc2224ed68a7446bf3986eb02bf0415751)
  * Add DPI Awareness for Tab images (Mixture of commits)
* Update a few test to use Office 2013 palettes
* Remove "redundant delegate constructors" for callbacks
* Fix "OnClick" routing for 
  - ListBox
  - CheckedListBox
  - TextBox
  - TreeView
* Update the test project to see if click on TextBox's work as expected 
* Set some private fields to "readonly"
* Fix AddToWorkspace in KryptonDockingManager
* Work out why clipping is the default for "DrawText" 
  - Applies to buttons, lLabels, Form Titles
  - Create test project - has theme selection, for type testing
* Remove 'Severity Code Description Project File Line Suppression State' Warning CS0618 'SecurityAction.RequestMinimum' is obsolete: 'Assembly level declarative security is obsolete and is no longer enforced by the CLR by default. See http://go.microsoft.com/fwlink/?LinkID=155570 for more information.' Basic Events 2015 [Source Path]\Krypton-NET-4.7.1\Source\Krypton Navigator Examples\Basic Events\Properties\AssemblyInfo.cs 35 Active
* An update to Component factory's KryptonToolkit to support the .NET 4.8 framework.
* Add generic c# .gitignore
* Change the solution to reflect Visual Studio 2017 usage
* Change Test apps to use .Net 4.8 Target framework
* Add designer dll to test apps to allow visual design and testing without GAC'ing
* Change Get Set functions to be inlined
* Merge Sequential Checks
* Clarify precedence with brackets
* Add braces to if statements
* Use explicit types instead of "vars"
* Object initialization can be simplified
* Delegate invocation can be simplified.
* Use pattern matching 
  - Adjust some logic to test bool before cast
  - Use of switch if necessary
* Variable declaration can be inlined
* Null check can be simplified
  - null-propagating code
* Local Variable can be const (And rename to upper case to follow the rest of the codebase.)
* ﻿Join declaration and assignment
* An update to Component factory's KryptonToolkit to support the .NET 4.8 framework.
* Add generic c# .gitignore
* Change the solution to reflect Visual Studio 2017 usage
* Change Test apps to use .Net 4.7.1 Target framework
* Add designer Dll to test apps to allow visual design and testing without GAC'ing
* Change Get Set functions to be inlined
* Merge Sequential Checks
* Clarify precedence with brackets
* Work out why clipping is the default for "DrawText" 
  - Applies to buttons, lLabels, Form Titles
  - Create test project - has theme selection, for type testing
* Remove Severity Code Description Project File Line Suppression State Warning CS0618 'SecurityAction.RequestMinimum' is obsolete: 'Assembly level declarative security is obsolete and is no longer enforced by the CLR by default. See http://go.microsoft.com/fwlink/?LinkID=155570 for more information.' Basic Events 2015 [Source Path]\Krypton-NET-4.7.1\Source\Krypton Navigator Examples\Basic Events\Properties\AssemblyInfo.cs 35 Active

## NOTE: This is a mirror of the Krypton-NET-4.70 repository, therefore it may take a day or two to update this repository with the .NET 4.8 framework. Thank you for your patience. 
