# Expense Report

## Summary

Introducing the <b>Expense Report Card</b>, a practical tool for handling expense requests. This card provides a <b>clear view</b> of each expense, with <b>easy expand and collapse</b> options for navigation. See who approved the expense, and stay informed with comments and attached files. Streamline your approval process and keep everything organized with this essential tool.

_bot-sent_ card example:

![picture of the extension in action](assets/expense-report-card.png)

## Compatibility

![Adaptive Card Version](https://img.shields.io/badge/Adaptive%20Card%20Version-1.5-green.svg)

## Solution

Solution|Author(s)
--------|---------
Expense Report | <a href="https://github.com/SuzanneTocco"><img align="center" width="28" height="28" src="https://wsrv.nl/?url=https://avatars.githubusercontent.com/u/149005128?v=4&w=36&h=36&fit=cover&mask=circle"></a> &nbsp; [Suz Tocco](https://github.com/SuzanneTocco) &nbsp;<a href="https://github.com/pabloas-ms"><img align="center" width="28" height="28" src="https://wsrv.nl/?url=https://avatars.githubusercontent.com/u/160079710?v=4&w=36&h=36&fit=cover&mask=circle"></a> &nbsp; [Pablo Vicente Astudillo Quintero](https://github.com/pabloas-ms) | Microsoft  

## Version history

Version|Date|Comments
-------|----|--------
1.0| January 15, 2025 | Initial release

### Disclaimer

_**THIS CODE IS PROVIDED _AS IS_ WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESS OR IMPLIED, INCLUDING ANY IMPLIED WARRANTIES OF FITNESS FOR A PARTICULAR PURPOSE, MERCHANTABILITY, OR NON-INFRINGEMENT.**_

## Responsive Layouts

This card utilizes our responsive framework, allowing for multiple layouts or content modifications for specific set width ranges. For more details on coding with this framework, see <a href="https://learn.microsoft.com/en-us/microsoftteams/platform/task-modules-and-cards/cards/cards-format?tabs=adaptive-md%2Cdesktop%2Cconnector-html#adaptive-card-responsive-layout">Design responsive Adaptive Cards</a>.

![Layouts](assets/card_layouts.png)


<br/><br/>

## 1) 👩‍🎨 Personalize This Card

### Step-by-step instructions and tips

#### 1) Copy the card JSON into the Designer Tool

Teams provides support for this tool, which is ideal for constructing and modifying cards. Copy the [card](card.json) payload and click on the <b>‘Open in Designer’</b> button to start working in the Designer platform.

_To create a "full width" card, add the following code to the JSON._ <br>

```json
"msTeams": {
  "width": "full"
}
```

<a href="https://dev.teams.microsoft.com/cards/new" target="_blank">
  <img src="../../assets/open_designer_button.png" width="190" alt="Open in Adaptive Card Designer" />
</a>

#### 2) Update Images

For thumbnail images, use a square aspect ratio. Save the image as a transparent PNG at 2x size to ensure high resolution across endpoints.
<b>Note:</b> You can add a radius to the image in the Designer to create slightly rounded edges.
  
* Update the image URL to link to your desired image.
* Update the image URL to link to the approving expense administrator.


#### 3) Connect to Proper Data

Ensure the card pulls the correct expense details.

#### 4) Update Button Copy and Actions

Customize button text and add or remove actions to suit your needs. <br>
If you wish to use icons in your button, you can choose from thousands of options in our Fluent icon library. Refer to the [Resources section](#resources--tools) on this page. 
<br>

<b>Note:</b> For other icons, use the color #818181 to ensure readability in both light and dark modes, or choose a color that you have verified looks good. Icons should fit edge-to-edge within a 16x16 square. Save them as transparent PNGs at 2x size for optimal resolution across different endpoints.
<br>

***For further design modifications** use the Microsoft Teams UI Kit in Figma to create, visualize, spec <a href="assets/expense-report-spec.png">(see current card spec)</a> , and verify the layouts before coding.<br />

<a href="https://www.figma.com/community/file/916836509871353159">
<img src="../../assets/teams_ui_kit_button.png" width="172" alt="Get the Microsoft Teams UI Kit" />
</a>

<br>

## 2) 🚗 Test Your Card

This is where the rubber meets the road to ensure high quality cards for all users across all endpoints. Road test your cards considering the following:

* <b>Themes:</b> Light Mode, Dark Mode, High Contrast
* <b>Common widths:</b> Chat, Channel, Meeting Chat, Phone (iOS- Portrait/landscape, Android-Portrait/landscape), Tablet (iOS- Portrait/landscape, Android-Portrait/landscape)
* <b>Accessibility:</b> Color contrast if creating new visuals, tabbing with keyboard or mobile equivelents, Voice assistance (readers to read card content)

<img src="../../assets/QAChecklist.png" alt="Open in Adaptive Card Designer" />

## Implementation Details

* We use responsive layout to move the text locations vertically so it's not squished in the `veryNarrow` width.

*  We use the `ToggleVisibility` action to show/hide additional information; notice also that we're toggling the caret icon as a way to dynamically represent the opened/closed state.

## Resources & Tools ##

* **Learn**: For complete details on how to design and build adaptive cards for your Teams app, visit the Microsoft Teams Learn website pages on  [Design Adaptive Cards for Your Teams App](https://learn.microsoft.com/en-us/microsoftteams/platform/task-modules-and-cards/cards/design-effective-cards?tabs=design) and [Build Cards](https://learn.microsoft.com/en-us/microsoftteams/platform/task-modules-and-cards/what-are-cards) (You can use the [schema explorer](https://adaptivecards.io/explorer/) to learn about the structure and options of each element.

* **Design**: Our tools can help you learn Teams patterns and design apps and cards.

  * Design Teams apps and cards with the [The Microsoft Teams UI Kit](https://www.figma.com/community/file/916836509871353159), which has core components, templates, and best practices.
 
  * Fluent icons are pre-built into the Designer and support both light and dark modes. You can choose from thousands of ready-to-use icons and select from a set of predefined colors. For more Fluent icon resources, check out [IconCloud](https://iconcloud.design/browse/Fluent%20System%20Library/Fluent%20Regular) or the [Fluent 2 Iconography site](https://fluent2.microsoft.design/iconography). <B>NOTE:</B> If you'd like to create custom icons, they should be saved as .pngs (export at 2x) and colored to ensure they look good in both light and dark modes.

* **Build**: Edit, build, preview, and test cards with our Teams Development Portal [Adaptive Card Designer](https://dev.teams.microsoft.com/cards).

</p>

## Contribute ##

Refer to the [contribution docs](/CONTRIBUTE.md) for more information.


