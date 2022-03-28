# Flutter Interview Questions with Answers

1. What is Flutter?
   
   Flutter is an open-source UI toolkit from Google for crafting beautiful, natively compiled applications for desktop, web, and mobile from a single codebase. Flutter apps are built using the Dart programming language. 

2. What is Dart?
   
	Dart is an object-oriented, garbage-collected programming language that you use to develop Flutter apps. It was also created by Google, but is open-source, and has community inside and outside Google. Dart was chosen as the language of Flutter for the following reason:

	Dart is AOT (Ahead Of Time) compiled to fast, predictable, native code, which allows almost all of Flutter to be written in Dart. This not only makes Flutter fast, virtually everything (including all the widgets) can be customized.

	Dart can also be JIT (Just In Time) compiled for exceptionally fast development cycles and game-changing workflow (including Flutter’s popular sub-second stateful hot reload).
	
	Dart allows Flutter to avoid the need for a separate declarative layout language like JSX or XML, or separate visual interface builders, because Dart’s declarative, programmatic layout is easy to read and visualize. And with all the layout in one language and in one place, it is easy for Flutter to provide advanced tooling that makes layout a snap.

3.	What is Cross-Platform?

	Software that can run on multiple types of computer systems like window, mac, android, ios, web etc..

4.	What is Widget?

	A Flutter app is always considered as a tree of widgets. Whenever you are going to code for building anything in Flutter, it will be inside a widget.
	
	Widgets describe how your app view should look like with their current configuration and state. When you made any alteration in the code, the widget rebuilt its description by calculating the difference of previous and current widget to determine the minimal changes for rendering in the app's UI.
	
	Widgets are nested with each other to build the app. It means your app's root is itself a widget, and all the way down is a widget also. For example, a widget can display something, can define design, can handle interaction, etc.

5.	 What are the two main types of widgets?
	<br>There are two types of widgets: 1.StatelessWidget : A widget that does not require mutable state. 2. StatefulWidget: A widget that has mutable state.

6.	What is the difference between the Stateless and the Stateful widgets?

	A Stateful widget has state information. It is referred to as dynamic because it can change the inner data during the widget lifetime. A widget that allows us to refresh the screen is called a Stateful widget. This widget does not have a build() method. It has createState() method, which returns a class that extends the Flutters State Class. The examples of the Stateful widget are Checkbox, Radio, Slider, InkWell, Form, and TextField.

	The Stateless widget does not have any state information. It remains static throughout its life-cycle. The examples of the Stateless widget are Text, Row, Column, Container, etc. If the screen or widget contains static content, it should be a Stateless widget, but if you want to change the content, it needs to be a Stateful widget.
7.	What are main and run app functions. How do they differ from each other?

	main () function came from Java-like languages so it's where all program started, without it, you can't write any program on Flutter.

	The runApp() function is responsible for returning the widgets that are attached to the screen as a root of the widget tree and will be rendered on the screen.
8.	What are MaterialApp and CupertinoApp widgets?

	Material widgets implements the Material design language for iOS, Android, and web.
	
	Cupertino widgets implements the current iOS design language based on Apple's Human Interface Guidelines.
9.	What is BuildContext?

	BuildContext in Flutter is the part of the widgets in the Element tree so that each widget has its own BuildContext. We mainly use it to get a reference to another widget or theme. For example, if we want to use a material design element, it is required to reference it to the scaffold. We can get it using the Scaffold.of(context) method.
10.	What are keys in Flutter?

	Keys in Flutter are used as an identifier for Widgets, Elements and SemanticsNodes. We can use it when a new widget tries to update an existing element; then, its key should be the same as the current widget key associated with the element. Keys should not be different amongst the Elements within the same parent.The subclasses of Key must be a GlobalKey or LocalKey. Keys are useful when we try to manipulate (such as adding, removing, or reordering) a collection of widgets of the same type that hold some state.
11.	What are Hot Restart and Hot Reload?
	
	Hot reload: It works with a small r key on the terminal or commands prompt. The hot reload feature allows us to quickly compile the newly added code in the file and sent them to Dart Virtual Machine (DVM). After DVM completes the updation, it immediately updates the UI of the app. It helps to build UI, add new features, fix bugs, and make app development fast.

	Hot Restart: It mainly works with States value. It allows developers to get a fully compiled application because it destroys the preserves State values and sets them to their defaults. On every Hot Restart, our app widget tree is completely rebuilt with the new typed code. It takes more time than Hot Reload to compile and update the app.
12.	How Tween animation works in Flutter?
		
	It is the short form of in-betweening. In a tween animation, it is required to define the start and endpoint of animation. It means the animation begins with the start value, then goes through a series of intermediate values and finally reached the end value. It also provides the timeline and curve, which defines the time and speed of the transition. The widget framework provides a calculation of how to transition from the start and endpoint.
13.	What are the advantages and disadvantages of Flutter?

	Flutter Pros:
	Cross-platform Development: This feature allows Flutter to write the code once, maintain, and can run on different platforms. It saves the time, effort, and money of the developers.

	Faster Development: The performance of the Flutter application is fast. Flutter compiles the application by using the arm C/C++ library that makes it closer to machine code and gives the app a better native performance.

	Good Community: Flutter has good community support where the developers can ask the issues and get the result quickly.

	Live and Hot Reloading: It makes the app development process extremely fast. This feature allows us to change or update the code are reflected as soon as the alterations are made.

	Minimal code: Flutter app is developed by Dart programming language, which uses JIT and AOT compilation to improve the overall start-up time, functioning and accelerates the performance. JIT enhances the development system and refreshes the UI without putting extra effort into building a new one.

	UI Focused: It has an excellent user interface because it uses a design-centric widget, high-development tools, advanced APIs, and many more features.

	Documentation: Flutter has very good documentation support. It is organized and more informative. We can get everything that we want to be written in one place.

	Flutter Cons:
	The apps made with Flutter tend to be weighty ones.

	Flutter-based apps are not supported by browsers as of now. This means no web apps.

	While Flutter is popular, it has not been around long enough to have a huge resource base. Therefore, your team will need to write a lot of stuff from scratch.

	Dart is not a popular language and if you want to work with Flutter you will have to learn how to use it.
14.	What are packages and plugins in Flutter?
		
	A package is a group of similar types of classes, interfaces, and sub-packages. The packages and plugins help us to build the app without having to develop everything from packages.
	
	In Flutter, it allows you to import new widgets or functionality into the app. The packages and plugins have a very small distinction. Generally, packages are the new components or the code written in dart languages, whereas plugins allow more functionality on the device by using the native code. In the DartPub, packages and plugins are both referred to as packages.
15.	What is pubspec.yaml file? Explain few elements of this file.
		
	It is the project's configuration file that will use a lot during working with the Flutter project. It allows you how your application works. It also allows us to set the constraints for the app. This file contains:
	
	Project general settings such as name, description, and version of the project.
	Project dependencies.
	Project assets (e.g., images, audio, etc.).
16.	What is an App state?
		
	State that is not ephemeral, that you want to share across many parts of your app, and that you want to keep between user sessions, is what we call application state (sometimes also called shared state).
	
	Examples of application state: - User preferences - Login info - Notifications in a social networking app - The shopping cart in an e-commerce app - Read/unread state of articles in a news app.
17.	What are the different build modes in Flutter?
		
	The Flutter tooling supports three modes when compiling your app, and a headless mode for testing.
	
	You choose a compilation mode depending on where you are in the development cycle.
	The modes are: - Debug - Profile - Release
18.	What is Fat Arrow Notation in Dart and when do you use it? 
		
	The fat arrow syntax is simply a short hand for returning an expression and is similar to  
	```
	(){
		return expression;
		}
	```

	The fat arrow is for returning a single line, braces are for returning a code block.
	Only an expression—not a statement—can appear between the arrow (=>) and the semicolon (;). For example, you can’t put an if statement there, but you can use a conditional expression
		
	// Normal function
	```
	void function1(int a) {
		  if (a == 3) {
    		print('arg was 3');
  			} else {
    		print('arg was not 3');
  			}
		}
	```
	// Arrow Function
	```
	void function2(int a) => print('this is arrow functin');
	```
19.	How is Flutter different from a WebView based application?
		
	Code you write for a WebView or an app that runs similarly has to go through multiple layers to finally get executed (like Cordova for Ionic). In essence, Flutter leapfrogs that by compiling down to native ARM code to execute on both platforms.
	
	“Hybrid” apps are slow, sluggish and look different from the platform they run on. Flutter apps run much, much faster than their hybrid counterparts.
	
	It’s much easier to access native components and sensors using plugins rather than using WebView which can’t take full use of their platform.
20.	When should you use WidgetsBindingObserver?  
		
	WidgetsBindingObserver should be used when we want to listen to the AppLifecycleState and call stop/start on our services.
21.	What is the difference between Expanded and Flexible widgets?  
		
	Expanded is just a shorthand for Flexible
	Using expanded this way:
	```
		Expanded(
 		child: Foo(),
		);
		is strictly equivalent to:
		Flexible(
 		fit: FlexFit.tight,
 		child: Foo(),
		);
	```
	You may want to use Flexible over Expanded when you want a different fit, useful in some responsive layouts.
	The difference between FlexFit.tight and FlexFit.loose is that loose will allow its child to have a maximum size while tight forces that child to fill all the available space.
22.	When to use main Axis Alignment and cross Axis Alignment?
			
	For Row:mainAxisAlignment = Horizontal AxiscrossAxisAlignment = Vertical Axis
	For Column: mainAxisAlignment = Vertical AxiscrossAxisAlignment = Horizontal Axis
23.	Where are the layout files? / Why doesn’t Flutter have layout files?
		
	In the Android framework, we separate an activity into layout and code. Because of this, we need to get references to views to work on them in Java. (Of course Kotlin lets you avoid that.) The layout file itself would be written in XML and consist of Views and ViewGroups.
	Flutter uses a completely new approach where instead of Views, you use widgets. A View in Android was mostly an element of the layout, but in Flutter, a Widget is pretty much everything. Everything from a button to a layout structure is a widget. The advantage here is in customisability. Imagine a button in Android. It has attributes like text which lets you add text to the button. But a button in Flutter does not take a title as a string, but another widget. Meaning inside a button you can have text, an image, an icon and pretty much anything you can imagine without breaking layout constraints. This also lets you make customised widgets pretty easily whereas in Android making customised views is a rather difficult thing to do.
24.	Isn’t drag-and-drop easier than making a layout in code?
		
	In some respect, that is true. But a lot of us in the Flutter community prefer the code way but that does not mean drag-and-drop is impossible to implement. If you completely prefer drag-and-drop, then Flutter Studio is a fantastic resource I’d recommend which helps you generate layouts from drag-and-drop. It’s a tool I’m genuinely impressed by and would love to see how it grows.
25.	Why are there Android and iOS folders in the Flutter project?

	There are three main folders in the Flutter project: lib, android and ios. ‘lib’ takes care of your Dart files. The Android and iOS folders exist to actually build an app on those respective platforms with the Dart files running on them. They also help you add permissions and platform-specific functionality to your project. When you run a Flutter project, it builds depending on which emulator or device it is running on, doing a Gradle or XCode build using the folders inside it. In short, those folders are entire apps which set the stage for the Flutter code to run.
26.	Why is my Flutter app so large?
		
	If you’ve run a Flutter application, you know it’s fast. Blazingly fast. How does it do that? When building an application, instead of only taking specific resources, it essentially takes all of them. Why does that help? Because if I change an icon from one to the other, it doesn't have to do a complete rebuild of the application. That’s why a Flutter debug build is so large. When a release build is created, only the needed resources are taken in and we get sizes we’re much more used to. Flutter apps will still be a tad bit larger than Android apps but it’s rather minuscule and plus the Flutter team is constantly looking for ways to reduce app size.
27.	Why does the first Flutter app build take so long?
		
	When building a Flutter app for the first time, a device-specific APK or IPA file is built. Hence, Gradle and XCode are used to build the files, taking time. The next time the app is restarted or hot-reloaded, Flutter essentially patches the changes on top of the existing app giving a blazing fast refresh.

	Note: The changes made with hot reload or restart ARE NOT SAVED on the device APK or IPA file. To ensure your app has all your changes on-device, consider stopping and running the app again.
28.	What does State mean? What is setState()?
		
	In simple terms, “State” is a collection of the variable values of your widget. Anything that can change like a counter count, text, etc. can be part of State. Imagine a counter app, the main dynamic thing is the counter count. When the count changes, the screen needs to be refreshed to display the new value. setState() is essentially a way of telling the app to refresh and rebuild the screen with the new values.
29.	Do you know what Ephemeral state means?  
		
	Ephemeral state (sometimes called UI state or local state) is the state you can neatly contain in a single widget.
30.	What is App state?
		
	State that is not ephemeral, that you want to share across many parts of your app, and that you want to keep between user sessions, is what we call application state (sometimes also called shared state).

31.	What are Null-aware operators?  
		
	Null-aware operators in dart allow you to make computations based on whether or not a value is null. It’s shorthand for longer expressions. A null-aware operator is a nice tool for making nullable types usable in Dart instead of throwing an error. ??
32.	Asynchronous programming: futures, async, await
		
	Asynchronous operations let your program complete work while waiting for another operation to finish.

	A future represents the result of an asynchronous operation, and can have two states: uncompleted or completed. Note: Uncompleted is a Dart term referring to the state of a future before it has produced a value.
	
	Uncompleted : When you call an asynchronous function, it returns an uncompleted future. That future is waiting for the function’s asynchronous operation to finish or to throw an error.
		
	Completed : If the asynchronous operation succeeds, the future completes with a value. Otherwise it completes with an error.
33.	Why do we pass functions to widgets?  
		
	Functions are first-class objects in Dart and can be passed as parameters to other functions. We pass a function to a widget essentially saying, invoke this function when something happens. Callbacks using interfaces like Android have too much boilerplate code for a simple callback. Dart does both declarations as well as setting up the callback. This becomes much cleaner and organized and helps us avoid unnecessary complications.
	```	
	FlatButton(  
  		onPressed: () {  
    	// Do something here  
  		});
	```
34.	What are Streams in Flutter/Dart?  
		
	Streams provide an asynchronous sequence of data. Data sequences include user-generated events and data read from files. You can process a stream using either await for or listen() from the Stream API. Streams provide a way to respond to errors. There are two kinds of streams: single subscription or broadcast.
35.	Why is the build method on State, and not StatefulWidget?
		
	Putting a Widget build(BuildContext context) method on State rather than putting a Widget build(BuildContext context, State state) method on StatefulWidget gives developers more flexibility when subclassing StatefulWidget.
36.	What is debug mode and when do you use it?
		
	In debug mode, the app is set up for debugging on the physical device, emulator, or simulator.
	
	Debug mode for mobile apps mean that: Assertions are enabled. Service extensions are enabled. Compilation is optimized for fast development and run cycles (but not for execution speed, binary size, or deployment). Debugging is enabled, and tools supporting source level debugging (such as DevTools) can connect to the process.
	
	Debug mode for a web app means that: The build is not minified and tree shaking has not been performed. The app is compiled with the dartdevc compiler for easier debugging.
37.	 Whats the difference between double.infinity and MediaQuery?
	<br>I want to be as big as my parent allows (double.infinity). I want to be as big as the screen (MediaQuery).

38.	What is profile mode and when do you use it?  
		
	In profile mode, some debugging ability is maintained—enough to profile your app’s performance. Profile mode is disabled on the emulator and simulator, because their behavior is not representative of real performance. On mobile, profile mode is similar to release mode, with the following differences:
	
	Some service extensions, such as the one that enables the performance overlay, are enabled.
	Tracing is enabled, and tools supporting source-level debugging (such as DevTools) can connect to the process.
	Profile mode for a web app means that:
	The build is not minified but tree shaking has been performed.
	The app is compiled with the dart2js compiler.
39.	Single subscription streams
		
	The most common kind of stream contains a sequence of events that are parts of a larger whole. Events need to be delivered in the correct order and without missing any of them. This is the kind of stream you get when you read a file or receive a web request. Such a stream can only be listened to once. Listening again later could mean missing out on initial events, and then the rest of the stream makes no sense. When you start listening, the data will be fetched and provided in chunks.

40.	Broadcast streams   
		
	The other kind of stream is intended for individual messages that can be handled one at a time. This kind of stream can be used for mouse events in a browser, for example. You can start listening to such a stream at any time, and you get the events that are fired while you listen. More than one listener can listen at the same time, and you can listen again later after canceling a previous subscription.

41.	 Explain Navigator Widget and its push/pop functions in Flutter?
	<br>The next few sections show how to navigate between two routes, using these steps:Create two routes:
	Navigate to the second route using Navigator.push(). 
	Return to the first route using Navigator.pop().

42.	Differentiate between named parameters and positional parameters in Dart?
	
	Dart's optional parameters are optional in that the caller isn't required to specify a value for the parameter when calling the function.
	Optional parameters can only be declared after any required parameters.

43.	What are keys in Flutter and when to use it?
		
	Flutter commonly uses keys when it needs to uniquely identify specific widgets within a collection. Using keys also helps Flutter preserve the state of StatefulWidget s while they're being replaced with other widgets or just moved in the widget tree.
44.	What is release mode and when do you use it?
		
	Use release mode for deploying the app, when you want maximum optimization and minimal footprint size. For mobile, release mode (which is not supported on the simulator or emulator), means that:
		
	Assertions are disabled.
	Debugging information is stripped out.
	Debugging is disabled.
	Compilation is optimized for fast startup, fast execution, and small package sizes.
	Service extensions are disabled.
	Release mode for a web app means that:
	The build is minified and tree shaking has been performed.
	The app is compiled with the dart2js compiler for best performance.

45.	What is the differences between required and optional parameters in DART?
		
	Dart's optional parameters are optional in that the caller isn't required to specify a value for the parameter when calling the function. Optional parameters can only be declared after any required parameters. Optional parameters can have a default value, which is used when a caller does not specify a value.
46.	How is whenCompleted() different from then() in Future?  
		
	whenComplete will fire a function either when the Future completes with an error or not, instead . then will fire a function after the Future completes without an error.
47.	How is InheritedWidget different from Provider?  
		
	If you use InheritedWidget in large application, build methods always rebuilds whole build method. But with Provider you have Consumer widget which is can be very specific to control specific blocks of build method, so you have more efficiency.
48.	What is the difference between Scaffold and Container in Flutter?  
		
	The Scaffold will give you a default struture properties like appbar, body, floatingaction button, drawer and many more to reduce your headache for creating a new custom structure yourself for your app activity/screen/page/UIView. While Container is a flexible widget with common properties any view will need.
49.	What is a difference between these operators ?? and ?.  
		
	??= assignment operator, which assigns a value to a variable only if that variable is currently null.
	
	a ??= 5;
	print(a); // <-- Still prints 3.

	Another null-aware operator is ??, which returns the expression on its left unless that expression’s value is null, in which case it evaluates and returns the expression on its right:

		print(1 ?? 3); // <-- Prints 1.
		print(null ?? 12); /

	Conditional property access:
	To guard access to a property or method of an object that might be null, put a question mark (?) before the dot (.):

50.	What does non-nullable by default mean in Dart?  
		
	The Dart language now supports sound null safety! When you opt into null safety, types in your code are non-nullable by default, meaning that variables can't contain null unless you say they can.

51.	What are Global Keys? 
 		
	 A key that is unique across the entire app. Global keys uniquely identify elements. Global keys provide access to other objects that are associated with those elements, such as BuildContext. For StatefulWidgets, global keys also provide access to State.
52.	What is a MediaQuery in Flutter and when do we use it?  
		
	MediaQuery provides a higher-level view of your app's screen size and can provide more detailed information about user layout preferences. In practice, MediaQuery is always there. You just access it by calling MediaQuery.
53.	Why is exit(0) not preferred for closing an app?  
		
	Close Android App With Code:
	
	exit(0) : This command also works but it is not recommended because it terminates the Dart VM process immediately and users may think that the app got crashed.
54.	JIT and AOT
		
	Dart Native (machine code JIT and AOT)
	During development, a fast developer cycle is critical for iteration. The Dart VM offers a just-in-time compiler (JIT) with incremental recompilation (enabling hot reload), live metrics collections (powering DevTools), and rich debugging support.
	
	When apps are ready to be deployed to production — whether you’re publishing to an app store or deploying to a production backend — the Dart AOT compiler enables ahead-of-time compilation to native ARM or x64 machine code. Your AOT-compiled app launches with consistent, short startup time.
		
	The AOT-compiled code runs inside an efficient Dart runtime that enforces the sound Dart type system and manages memory using fast object allocation and a generational garbage collector.
55.	What is the purpose of SafeArea in Flutter?
		
	A widget that insets its child by sufficient padding to avoid intrusions by the operating system. For example, this will indent the child by enough to avoid the status bar at the top of the screen.
56.	Why should you use kReleaseMode instead of assert?  
		
	Generally it is better to use kDebugMode or assert to gate code, since using kReleaseMode will introduce differences between release and profile builds, which makes performance testing less representative.
57.	What's the difference between async and async* in Dart?  
		
	Marking a function as async or async* allows it to use the async/await for a Future.

	The difference between both is that async* will always return a Stream and offer some syntactical sugar to emit a value through the yield keyword.

	We can therefore do the following:

	```
	Stream<int> foo() async* {
  		for (int i = 0; i < 42; i++) {
    	await Future.delayed(const Duration	(seconds: 1));
    		yield i;
  			}
		}
	```
	This function emits a value every second, which increments every time.
58.	What does a class with a method named ._() mean in Dart/Flutter?  
		
	AppTheme._(); is a named constructor (another examples might be the copy constructor on some objects in the Flutter framework: ThemeData.copy(...);).
	
	In dart, if the leading character is an underscore, then the function/constructor is private to the library. That's also the case here, and the underscore is also the only character, so I'd imagine whoever wrote this constructor didn't plan for that constructor to ever be called at all.
	
	The AppTheme._(); isn't necessary unless you don't want AppTheme to ever be accidentally instantiated using the implicit default constructor.