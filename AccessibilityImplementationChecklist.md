I use this checklist to make sure I've not forgotten anything when I'm implementing VoiceOver support.<br/>
I do this per-screen, for all of the screens in the app.<br/>
Not all of the items in the checklist apply to all screens.

__VoiceOver Implementation Checklist__
- [ ] Explore existing VoiceOver functionality before doing anything
- [ ] Add accessibilityIdentifier
- [ ] Add accessibilityLabel
- [ ] Change accessibilityLabel if the UI element state changes
- [ ] Add accessibilityHint
- [ ] Enclose icon buttons and associated labels in a container view
- [ ] Set isAccessibilityElement to NO for UI elements which should not be announced
- [ ] Use isAccessibilityElement for container views
- [ ] If there is a UILabel and then a text view associated with it, set the text view's accessibilityLabel equal to the text of the label. Then, set isAccessibilityElement = NO on the label.
- [ ] Modify swipe order if needed using UIAccessibilityContainer methods
- [ ] UITableView - Add UIAccessibilityTraitButton to cells
- [ ] UITableView - Add UIAccessibilityTraitSelected to cells with a checkmark accessoryType
- [ ] UITableView - Cells with UISwitch should announce the switch state.
- [ ] UITableView - Determine if section headers should be an accessibilityElement. In some cases the section header should not be announced.
- [ ] UINavigationController title - To set custom VoiceOver text, set the view controller's navigationItem.accessibilityLabel
- [ ] UISegmentedControl - To set custom VoiceOver text for the segments, set the NSString accessibilityLabel for each segment title.
- [ ] UIActivityIndicatorView - Set hidesWhenStopped = YES to prevent VoiceOver from announcing the activity indicator when it is stopped
- [ ] Change focus to the back button when drilling down
- [ ] Post UIAccessibilityLayoutChangedNotification for UI updates
- [ ] Post UIAccessibilityScreenChangedNotification on screen transitions
- [ ] Unit test accessibilityIdentifier
- [ ] Unit test accessibilityLabel
- [ ] Unit test accessibilityLabel changes
- [ ] Unit test accessibilityHint
- [ ] Unit test isAccessibilityElement
- [ ] Unit test accessibilityTraits
- [ ] UI test - use accessibilityIdentifier where possible. Remember UIBarButtonItem does not implement accessibilityIdentifier properly. Do not use for finding this element.
