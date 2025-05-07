# Checklist: Dynamic Updates, AJAX, and Single-page Applications

## Summary

### Dynamic Content

Silence is bad. When screen reader users activate a feature (link, button, control, etc.), or when an important part of the content changes, they need to hear feedback. One of the basic challenges with dynamic content is to figure out the best way to tell screen reader users about the dynamic changes. The three main options are:

1. **Load or reload the page,** with the page `<title>` reflecting the updated dynamic information.
2. **Move the focus** to the updated content or to a confirmation or error message.
3. **Use an ARIA live region** to make an announcement.

### Time limits
Make sure to give users enough time to complete tasks, or to warn them when their time is about to expire, preferably giving them the option to extend their time. Don't automatically refresh or reload the page.

### AJAX
Inform users (generally by moving the focus or using ARIA live regions) when new is loaded at the user's request (such as clicking on a link or button), but be careful to not announce too frequently, as in the case of lazy loading, and be sure to construct the UX ina way that allows keyboard users to reach all parts of the page (be careful with infinite scrolling).

## Checklist

### Notifying Users of Changes

#### Status Messages

- [ ] Status messages <mark>**MUST**</mark> be programmatically determinable through role or properties such that they can be presented to the user by assistive technologies without receiving focus.

### Time Limits

#### Session Timeout

- [ ] If there is a session time limit, users <mark>**MUST**</mark> be warned before the session ends and <mark>**MUST**</mark> be given time to save their data and/or extend the session.
- [ ] Incomplete data **SHOULD** be saved after a session timeout.
  - [ ] Users **SHOULD** be warned of the duration of any user inactivity that could cause data loss, unless the data is preserved for more than 20 hours when the user does not take any actions.

#### Timers with Fixed Deadlines

- [ ] Timers with fixed deadlines **SHOULD** provide users with a dynamic countdown feature, especially if the deadline is soon.
- [ ] Countdown features **SHOULD** post ARIA live announcements at strategic intervals.
- [ ] Countdown features <mark>**MUST NOT**</mark> post ARIA live so frequently that they become overwhelming to screen reader users.
- [ ] If the timing is critical, a dynamic countdown MAY be included in the page `<title>`.
- [ ] If the timing is critical, the dynamic countdown timers and alerts **SHOULD** be included across all relevant pages on the site.

#### Auto Refresh/Reload

- [ ] The page <mark>**MUST NOT**</mark> refresh or reload automatically.
- [ ] A web page MAY notify the user when a refresh is recommended.

### AJAX

#### Lazy Loading

- [ ] Placeholders for AJAX content **SHOULD** inform screen reader users that the content is loading.
- [ ] "Lazy loading" AJAX content **SHOULD NOT** be announced as it loads.

#### Infinite Scrolling

- [ ] An "infinite scrolling" feature <mark>**MUST**</mark> allow users to reach all areas of the page with the keyboard.
- [ ] An "infinite scrolling" feature MAY be activated only at the user's request.

#### Interstitial Views

- [ ] Screen reader users <mark>**MUST**</mark> be informed when a webpage launches an interstitial view, a progress indicator, or enters into a paused or busy state.

#### Single Page Applications

- [ ] Screen reader users <mark>**MUST**</mark> be made aware when new "pages" are loaded in single-page applications.
- [ ] The browser history <mark>**MUST**</mark> be updated when an AJAX event is the result of clicking on a link OR if the event is such that a user would expect to be able to use the "back" button after the event.
- [ ] The page <mark>**MUST**</mark> respond appropriately when the user activates back or forward functionality in the browser.

