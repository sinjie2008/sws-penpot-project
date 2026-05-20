# Shared Naming Rules

Use clear, readable names for boards, groups, and layers.

---

## Section board naming

Use numbered section board names:

```text
01_Header_Board
02_Breadcrumb_Board
03_Sub_Navigation_Board
04_Hero_Banner_Board
05_Introduction_Board
06_Overview_Board
07_Product_Categories_Board
08_Industries_We_Serve_Board
09_Quality_Certified_Performance_Assured_Board
10_Latest_News_Board
11_Regional_Support_Board
12_CTA_Board
13_Footer_Board
```

Only create boards that actually exist in the target board.
Do not invent missing sections.
Do not create empty boards.

If the target board has different sections, rename based on the actual visible content.

---

## Important separation rule

Breadcrumb must be its own board if it exists.
Sub Navigation must be its own board if it exists.

Do not merge Breadcrumb into Header.
Do not merge Breadcrumb into Hero.
Do not merge Sub Navigation into Header.
Do not merge Sub Navigation into Hero.
Do not merge Sub Navigation into Main Content.

---

## Group naming

Use clear group names ending with `_Group`.

Examples:

```text
Header_Logo_Group
Header_Navigation_Group
Header_Action_Group
Hero_Content_Group
Hero_Primary_Button_Group
Breadcrumb_Group
Sub_Navigation_Group
Industry_Card_Automotive_Group
Latest_News_Card_01_Group
Footer_Contact_Group
Footer_Quick_Links_Group
```

---

## Layer naming

Rename unclear layers into meaningful names.

Avoid:

```text
Rectangle 123
Group 45
Image 8
Text 90
Path 12
```

Use:

```text
Header_Logo
Header_Navigation_Item_Products
Hero_Title
Hero_Subtitle
Hero_Image_Placeholder
Latest_News_Card_01_Title
Footer_Copyright
```

Do not change actual visible text content.
Only rename the layer name.
