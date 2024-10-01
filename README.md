# JOBSHEET 5 TUGAS PRAKTIKUM NO 4

Nama: Wulan Maulidya P. F

Kelas: TI-3H

No. Absen: 27

NIM: 2241720174

---

## 4. Selesaikan Codelabs: Your first Flutter app, lalu buatlah laporan praktikumnya dan push ke repository GitHub Anda!

### Make new project, and name your project something like namer_app or my_awesome_namer.

![Tugas 4](/images/tgs_no4a.png)

### In the left pane of VS Code, make sure that Explorer is selected, and open the pubspec.yaml file. Replace the contents of this file with the following:

![Tugas 4](/images/tgs_no4b.png)

### Next, open another configuration file in the project, analysis_options.yaml. Replace its contents with the following:

![Tugas 4](/images/tgs_no4c.png)

### Finally, open the main.dart file under the lib/ directory. Replace the contents of this file with the following:

![Tugas 4](/images/tgs_no4d.png)

### Launch the app. First, open lib/main.dart and make sure that you have your target device selected. At the bottom right corner of VS Code, you'll find a button that shows the current target device. Click to change it. While lib/main.dart is open, find the "play" button in the upper right-hand corner of VS Code's window, and click it. After about a minute, your app launches in debug mode. It doesn't look like much yet

![Tugas 4](/images/tgs_no4e.png)

### First Hot Reload. At the bottom of lib/main.dart, add something to the string in the first Text object, and save the file (with Ctrl+S or Cmd+S). For example:

![Tugas 4](/images/tgs_no4f.png)

### Adding a button. Next, add a button at the bottom of the Column, right below the second Text instance.

![Tugas 4](/images/tgs_no4g.png)

### A Flutter crash course in 5 minutes. As much fun as it is to watch the Debug Console, you want the button to do something more meaningful. Before getting to that, though, take a closer look at the code in lib/main.dart, to understand how it works. At the very top of the file, you'll find the main() function. In its current form, it only tells Flutter to run the app defined in MyApp.

![Tugas 4](/images/tgs_no4h.png)

### The MyApp class extends StatelessWidget. Widgets are the elements from which you build every Flutter app. As you can see, even the app itself is a widget. The code in MyApp sets up the whole app. It creates the app-wide state (more on this later), names the app, defines the visual theme, and sets the "home" widget—the starting point of your app.

![Tugas 4](/images/tgs_no4i.png)

### Next, the MyAppState class defines the app's...well...state. This is your first foray into Flutter, so this codelab will keep it simple and focused. There are many powerful ways to manage app state in Flutter. One of the easiest to explain is ChangeNotifier, the approach taken by this app.

![Tugas 4](/images/tgs_no4j.png)

### Your first behavior. Scroll to MyAppState and add a getNext method.

![Tugas 4](/images/tgs_no4k.png)

### All that remains is to call the getNext method from the button's callback.

![Tugas 4](/images/tgs_no4l.png)

### Extract a widget. For that reason, rewrite the MyHomePage widget as follows:

![Tugas 4](/images/tgs_no4m.png)

### Now, call up the Refactor menu. Right click the piece of code you want to refactor (Text in this case) and select Refactor... from the drop-down menu

![Tugas 4](/images/tgs_no4n.png)

### In the Refactor menu, select Extract Widget. Assign a name, such as BigCard, and click Enter.

![Tugas 4](/images/tgs_no4o.png)

### This automatically creates a new class, BigCard, at the end of the current file. The class looks something like the following:

![Tugas 4](/images/tgs_no4p.png)

### Add a Card. Instead, select Wrap with Padding. This creates a new parent widget around the Text widget called Padding. After saving, you'll see that the random word already has more breathing room.

![Tugas 4](/images/tgs_no4q.png)

### Next, go one level higher. Place your cursor on the Padding widget, pull up the Refactor menu, and select Wrap with widget.... This allows you to specify the parent widget. Type "Card" and press Enter.

![Tugas 4](/images/tgs_no4r.png)

### This wraps the Padding widget, and therefore also the Text, with a Card widget.

![Tugas 4](/images/tgs_no4s.png)

_When Click The Button:_

![Tugas 4](/images/tgs_no4t.png)

### Theme and style. Make the following changes to BigCard's build() method.

![Tugas 4](/images/tgs_no4u.png)

### TextTheme. The card still has a problem: the text is too small and its color is hard to read. To fix this, make the following changes to BigCard's build() method.

![Tugas 4](/images/tgs_no4v.png)

### Improve accessibility. Use Text's semanticsLabel property to override the visual content of the text widget with a semantic content that is more appropriate for screen readers:

![Tugas 4](/images/tgs_no4w.png)

### Center the UI. First, remember that BigCard is part of a Column. By default, columns lump their children to the top, but we can easily override this. Go to MyHomePage's build() method, and make the following change:

![Tugas 4](/images/tgs_no4x.png)

### You can just center the column itself. Put your cursor onto Column, call up the Refactor menu (with Ctrl+. or Cmd+.), and select Wrap with Center.

![Tugas 4](/images/tgs_no4y.png)

### With the optional changes, MyHomePage contains this code:

![Tugas 4](/images/tgs_no4z.png)

### Add the business logic

![Tugas 4](/images/tgs_no4z1.png)

### Add the button

![Tugas 4](/images/tgs_no4z2.png)

### Here's one way to add the second button to MyHomePage

![Tugas 4](/images/tgs_no4z3.png)

_When Click The Button:_

![Tugas 4](/images/tgs_no4z4.png)

### Select all of MyHomePage, delete it, and replace with the following code:

![Tugas 4](/images/tgs_no4z5.png)

### You can change the extended: false line in NavigationRail to true. This shows the labels next to the icons. In a future step, you will learn how to do this automatically when the app has enough horizontal space.

![Tugas 4](/images/tgs_no4z6.png)

### Stateless versus stateful widgets. Place your cursor on the first line of MyHomePage (the one that starts with class MyHomePage...), and call up the Refactor menu using Ctrl+. or Cmd+.. Then, select Convert to StatefulWidget.

![Tugas 4](/images/tgs_no4z7.png)

### setState. The new stateful widget only needs to track one variable: selectedIndex. Make the following 3 changes to \_MyHomePageState:

![Tugas 4](/images/tgs_no4z8.png)

_When Click The Favourites Bar:_

![Tugas 4](/images/tgs_no4z9.png)

### Use selectedIndex. Place the following code at the top of \_MyHomePageState's build method, just before return Scaffold:

![Tugas 4](/images/tgs_no4z10.png)

### Here's \_MyHomePageState after that single remaining change:

![Tugas 4](/images/tgs_no4z11.png)

_When Click The Favourites Bar:_

![Tugas 4](/images/tgs_no4z12.png)

### Responsiveness. Inside \_MyHomePageState's build method, put your cursor on Scaffold. Next, Call up the Refactor menu with Ctrl+. (Windows/Linux) or Cmd+. (Mac). Next, Select Wrap with Builder and press Enter. Next, Modify the name of the newly added Builder to LayoutBuilder. Last, Modify the callback parameter list from (context) to (context, constraints).

![Tugas 4](/images/tgs_no4z13.png)

### Now your code can decide whether to show the label by querying the current constraints. Make the following single-line change to \_MyHomePageState's build method:

![Tugas 4](/images/tgs_no4z14.png)

_When Changing The Screen Size:_

![Tugas 4](/images/tgs_no4z15.png)

### Add New Page. Here's the new FavoritesPage class:

![Tugas 4](/images/tgs_no4z16.png)

_When Click The Like Button & Favourites Bar:_

![Tugas 4](/images/tgs_no4z17.png)
