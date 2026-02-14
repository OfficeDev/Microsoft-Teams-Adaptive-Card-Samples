# Team Standup Summary

## Summary

The **Team Standup Summary Card** provides a quick overview of your team's daily standup status. It displays each team member's progress, blockers, and current tasks in a **responsive grid layout** that adapts from a 2-column grid on desktop to a single-column stack on mobile. A highlighted blocker summary ensures critical issues get immediate visibility.

_bot-sent_ card example:

![picture of the extension in action](assets/team-standup-summary-card.png)

## Compatibility

![Adaptive Card Version](https://img.shields.io/badge/Adaptive%20Card%20Version-1.5-green.svg)

## Solution

Solution|Author(s)
--------|---------
Team Standup Summary | <a href="https://github.com/VikrantSingh01"><img align="center" width="28" height="28" src="https://wsrv.nl/?url=https://avatars.githubusercontent.com/u/VikrantSingh01?v=4&w=36&h=36&fit=cover&mask=circle"></a> &nbsp; [Vikrant Singh](https://github.com/VikrantSingh01)

## Version history

Version|Date|Comments
-------|----|--------
1.0| February 14, 2026 | Initial release

### Disclaimer

_**THIS CODE IS PROVIDED _AS IS_ WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESS OR IMPLIED, INCLUDING ANY IMPLIED WARRANTIES OF FITNESS FOR A PARTICULAR PURPOSE, MERCHANTABILITY, OR NON-INFRINGEMENT.**_

## Responsive Layouts

This card utilizes the responsive framework, allowing for multiple layouts and content modifications for specific width ranges. For more details on coding with this framework, see <a href="https://learn.microsoft.com/en-us/microsoftteams/platform/task-modules-and-cards/cards/cards-format?tabs=adaptive-md%2Cdesktop%2Cconnector-html#adaptive-card-responsive-layout">Design responsive Adaptive Cards</a>.

### Layout Breakpoints

| Width | Layout | Description |
|---|---|---|
| **VeryNarrow** | Single column stack | Team members stack vertically; sprint info collapses to separate lines |
| **Narrow** | Single column stack | Team members stack vertically; sprint info shows side-by-side |
| **Standard+** | 2x2 grid | Team member cards displayed in a 2-column grid via `Layout.AreaGrid` |

### Responsive Features Used

- **`Layout.AreaGrid`** with `targetWidth: "atLeast:Standard"` — switches between 2-column grid and default stack layout
- **`targetWidth: "VeryNarrow"`** on elements — shows condensed header layout for very narrow screens
- **`targetWidth: "AtLeast:Narrow"`** on elements — shows inline sprint info on wider screens
- **`Badge`** component — visual status indicators (On track, Blocked, Not reported)

<br/><br/>

## 1) Personalize This Card

### Step-by-step instructions and tips

#### 1) Copy the card JSON into the Designer Tool

Copy the [card](card.json) payload and click on the **'Open in Designer'** button to start working in the Designer platform.

_To create a "full width" card, add the following code to the JSON._

```json
"msTeams": {
  "width": "full"
}
```

<a href="https://dev.teams.microsoft.com/cards/new" target="_blank">
  <img src="../../assets/open_designer_button.png" width="190" alt="Open in Adaptive Card Designer" />
</a>

#### 2) Update Team Members

Replace the team member names, avatars, and status updates with your actual team data.

#### 3) Connect to Your Data Source

Integrate with your standup bot or project management tool to automatically populate daily updates.

#### 4) Update Button Actions

Customize the "View sprint board" and "Submit update" buttons to link to your team's actual tools.

## 2) Test Your Card

Road test your cards considering the following:

* **Themes:** Light Mode, Dark Mode, High Contrast
* **Common widths:** Chat, Channel, Meeting Chat, Phone (iOS - Portrait/landscape, Android - Portrait/landscape), Tablet (iOS - Portrait/landscape, Android - Portrait/landscape)
* **Accessibility:** Color contrast, keyboard tabbing, voice assistance

## Implementation Details

* We use `Layout.AreaGrid` on the team member container to show a **2x2 grid** on Standard+ widths and fall back to `Layout.Stack` on Narrow/VeryNarrow widths.
* The header row uses **dual rendering**: a `ColumnSet` for Narrow+ and a stacked `Container` for VeryNarrow, ensuring the team name and badge don't get squished.
* The sprint footer similarly adapts: side-by-side on Narrow+ and stacked on VeryNarrow.
* The blocker summary container uses the `attention` style to visually highlight urgent issues.

## Resources & Tools

* **Learn**: [Design Adaptive Cards for Your Teams App](https://learn.microsoft.com/en-us/microsoftteams/platform/task-modules-and-cards/cards/design-effective-cards?tabs=design) and [Build Cards](https://learn.microsoft.com/en-us/microsoftteams/platform/task-modules-and-cards/what-are-cards)
* **Design**: [The Microsoft Teams UI Kit](https://www.figma.com/community/file/916836509871353159)
* **Build**: [Adaptive Card Designer](https://dev.teams.microsoft.com/cards)

## Contribute

Refer to the [contribution docs](/CONTRIBUTE.md) for more information.
