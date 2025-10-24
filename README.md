This is a minimal project demonstrating issues hot-reloading DataTemplate elements in Noesis.

This project was creating in response to an issue observed in Unity 6000.2.7f2 with version 3.2.9 of the Noesis plugin.

## Repro Steps
1. Open Project in Noesis Studio 1.243-beta or earlier
2. Open the Resources panel
3. Edit "[SubViewModel default]"
4. Change something in the template (text or grid color)
5. Return to the MainPage.xaml view

## Expected
The main page should show the updated template (e.g. background changed from red to blue)

## Actual
The main page continues to show the old template.

Changing the MainPage.xaml outside of Noesis Studio will trigger a hot reload at this time, correcting the rendering.

In Unity, changing the xaml will NOT trigger a hot reload. Instead you must exit and re-enter playmode.