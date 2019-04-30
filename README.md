# Off the Record
Off the Record is the Hotchkiss Record's Newsletter, distributed bi-weekly on the off-weeks of the print run to the student body as well as subscribers. 

## Installation
Off the Record is compiled in [`mjml`](https://mjml.io/), using [`node.js`](https://nodejs.org/en/). It is sent as HTML embed within an email. To set up the environment––run
```shell
git clone https://github.com/TheHotchkissRecord/offtherecord.git
```
or use the local GitHub client to clone the repo in your desired directory. Initiate the necessary packages and dependencies:
```shell
npm init -y && npm install mjml
```
```shell
export PATH="$PATH:./node_modules/.bin"
```
(*You might need to [install](https://nodejs.org/en/) node & npm onto your device first.*)

## Documentation
An *Off the Record* mjml document is initiated as such: 
```html
<mjml>
  <mj-head>
    <!-- Title and Date --> 
    <mj-title>Off the Record - April 29, 2019</mj-title>
    <!-- Description --> 
    <mj-preview>~Description</mj-preview>
    <mj-attributes>
      <mj-all font-family="'Helvetica Neue', Helvetica, Arial, sans-serif"></mj-all>
      <mj-text font-weight="400" font-size="16px" color="#000000" line-height="24px" font-family="'Helvetica Neue', Helvetica, Arial, sans-serif"></mj-text>
    </mj-attributes>
    <mj-style inline="inline">
      .body-section { -webkit-box-shadow: 1px 4px 11px 0px rgba(0, 0, 0, 0.15); -moz-box-shadow: 1px 4px 11px 0px rgba(0, 0, 0, 0.15); box-shadow: 1px 4px 11px 0px rgba(0, 0, 0, 0.15); }
    </mj-style>
    <mj-style inline="inline">
      .text-link { color: #5e6ebf }
    </mj-style>
    <mj-style inline="inline">
      .footer-link { color: #888888 }
    </mj-style>
  </mj-head>
  <mj-body background-color="#E7E7E7" width="600px">
    <!-- BODY CONTENT --> 
  </mj-body>
</mjml>
```

The header, which includes the logo, the date, and the address is involves an `mj-section` block (This is the first thing in the **body content** block): 
```html
<mj-section full-width="full-width" background-color="#02174c" padding-bottom="0">
  <mj-column width="100%">
    <mj-image src="https://graphics.thehr.org/newsletter/offtherecord_dark.png" alt="" align="center" width="400px" />
    <mj-text color="#ffffff" font-weight="bold" align="center" text-transform="uppercase" font-size="16px" letter-spacing="1px" padding-top="30px">
      <!-- Date -->
      Monday, April 29, 2019
      <br/>
      <span style="color: #979797; font-weight: normal">-</span>
    </mj-text>
    <mj-text color="#17CBC4" align="center" font-size="13px" padding-top="0" font-weight="bold" text-transform="uppercase" letter-spacing="1px" line-height="30px">
      Lakeville, CT
    </mj-text>
    <mj-text></mj-text>
  </mj-column>
</mj-section>
```

The `mj-wrapper` wraps the main content of the newsletter (this goes after the header section): 
```html
<mj-wrapper padding-top="0" padding-bottom="0" css-class="body-section">
<!-- TEXT CONTENT -->
</mj-wrapper>
```

The editorial message goes in next (in the **text content**): 
```html
<mj-section background-color="#ffffff" padding-left="15px" padding-right="15px">
  <mj-column width="100%">
    <mj-text color="#637381" font-size="16px">
      <!-- Editorial Message -->
      <br /><br /> - <i>The Record Editorial Board</i>
    </mj-text>
  </mj-column>
</mj-section>
```

Afterward, article previews are implemented as article blocks. As many of these blocks can go in after the editorial message: 
```html
<!-- Start of an article preview -->
<mj-section full-width="full-width" background-color="#ffffff" padding-bottom="0">
  <mj-column width="100%">
    <mj-image src="https://newsletter.thehr.org/thumbnail.png" width="600px" alt="" padding="0" href="https://hotchkissrecord.org/yyyy/mm/article-link/" />
  </mj-column>
</mj-section>
<!-- Start of text -->
<mj-section background-color="#ffffff" padding-left="15px" padding-right="15px">
  <mj-column width="100%">
    <mj-text color="#637381" font-size="12px" align=right padding-right="5px">
      <i> <!-- Caption --> </i>
    </mj-text>
    <mj-text color="#212b35" font-weight="bold" font-size="20px">
      <!-- Title -->
    </mj-text>
    <mj-text color="#212b35" font-size="12px" height=15px font-weight="bold">
      <!-- Byline + Author -->
    </mj-text>
    <mj-text color="#637381" font-size="16px">
      <!-- Article Preview -->
    </mj-text>
    <mj-button background-color="#202F5A" align="center" color="#ffffff" font-size="17px" font-weight="bold" href="https://hotchkissrecord.org/yyyy/mm/article-link/" width="300px">
      Continue Reading
    </mj-button>
  </mj-column>
</mj-section>
<!-- End of text-->
<!-- End of an article -->
```

After all the articles are in, place the footer of the email in: (nothing should change from here)
```html
<mj-section>
  <mj-column width="100%" padding="0">
    <mj-social font-size="15px" icon-size="30px" mode="horizontal" padding="0" align="center">
      <mj-social-element name="instagram" href="https://www.instagram.com/hotchkissrecord/" background-color="#A1A0A0">
      </mj-social-element>
      <mj-social-element name="web" href="https://hotchkissrecord.org/" background-color="#A1A0A0">
      </mj-social-element>
    </mj-social>
    <mj-text color="#445566" font-size="11px" font-weight="bold" align="center">
      <a href="https://newsletter.thehr.org/20190429/index.html">View this email in your browser</a>
    </mj-text>
    <mj-text color="#445566" font-size="11px" align="center" line-height="16px">
      Copyright © 2019 The Hotchkiss Record, All rights reserved. You are receiving this email because you are a member of the Hotchkiss community.
    </mj-text>
    <mj-text color="#445566" font-size="11px" align="center" line-height="16px">
      <b>Our mailing address is:</b><br /> The Hotchkiss Record <br /> 11 Interlaken Rd <br /> Lakeville, CT 06039-2141
    </mj-text>
  </mj-column>
</mj-section>
<mj-section padding-top="0">
  <mj-group>
    <mj-column width="100%" padding-right="0">
      <mj-text color="#445566" font-size="11px" align="center" line-height="16px" font-weight="bold">
      </mj-text>
    </mj-column>
  </mj-group>
</mj-section>
```

Now that the newsletter is assembled, you can compile into an HTML file from the command line: 
```shell
mjml -r yyyymmdd/newsletter.mjml -o yyyymmdd/index.html
```

## To-Do
 - Create automation to build newsletter automatically. 
