<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">
<html>
<head>
  <meta http-equiv="Content-Type" content="text/html; charset=utf-8">
  <title>Script Upgrade | QRCDR - QRcode generator</title>
<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css" integrity="sha384-ggOyR0iXCbMQv3Xipma34MD+dH/1fQ784/j6cY/iJTQUOhcWr7x9JvoRxT2MZw1T" crossorigin="anonymous">
</head>
<body>
<div class="container">
  <div class="row">
  <div class="col-md-12 py-4 mt-4">
    <div class="alert alert-primary">
      <h2>QRCDR 5.2.8 to 5.2.9</h2>
      <p>Files updated:</p>
      <ul>
        <li>/lib/class-qrcdr.php</li>
      </ul>

      <h2>QRCDR 5.2.7 to 5.2.8</h2>
      <p>Files updated:</p>
      <ul>
        <li>index.php</li>
        <li>/ajax/png.php</li>
        <li>/ajax/process.php</li>
        <li>/lib/class-qrcdr.php</li>
        <li>/pdf/index.php</li>
        <li>/template/footer.php</li>
      </ul>
      <p>New files added:</p>
      <ul>
        <li>/template/_privacy.html</li>
        <li>/template/_terms.html</li>
        <li>/template/example.html</li>
        <li>/template/modals.php</li>
      </ul>
      <p>Also update the translations inside the folder /translations/</p>

    </div>


      <h2>QRCDR 5.2.6 to 5.2.7</h2>
      <p>Files updated:</p>
      <ul>
        <li>index.php</li>
        <li>/ajax/create.php</li>
        <li>/js/qrcdr.js</li>
        <li>/js/qrcdr.min.js</li>
        <li>/lib/class-qrcdr.php</li>
        <li>/lib/EasySVG.php</li>
      </ul>
      <p>New file added:</p>
      <ul>
        <li>/lib/fonts/ZCOOLKuaiLe-Regular.svg</li>
      </ul>

<hr>

      <h2>QRCDR 5.2.5 to 5.2.6</h2>
      <p>Files updated:</p>
      <ul>
        <li>index.php</li>
        <li>/js/qrcdr.js</li>
        <li>/js/qrcdr.min.js</li>
      </ul>

<hr>

      <h2>QRCDR 5.2.4 to 5.2.5</h2>
      <p>Files updated:</p>
      <ul>
        <li>index.php</li>
        <li>style.css</li>
        <li>/ajax/process.php</li>
        <li>/include/ (replace the whole folder)</li>
        <li>/lib/ (replace the whole folder)</li>
        <li>/translations/de.php</li>
        <li>/translations/zh.php</li>
      </ul>

<hr>

      <h2>QRCDR 5.2.3 to 5.2.4</h2>
      <p>Files updated:</p>
      <ul>
        <li>index.php</li>
        <li>/ajax/process.php</li>
        <li>/lib/class-qrcdr.php</li>
      </ul>

<hr>

      <h2>QRCDR 5.2.2 to 5.2.3</h2>
      <p>Follow the <a href="#generic-upgrade">GENERIC SCRIPT UPGRADE</a></p>
      <p>Also update the translations inside the folder /translations/</p>

<hr>

      <h2>QRCDR 5.1.x to 5.2</h2>
      <p>Follow the <a href="#generic-upgrade">GENERIC SCRIPT UPGRADE</a></p>
      <p>Also update the translations inside the folder /translations/</p>

<hr>

      <h2>QRCDR 4.x to 5</h2>
      <p>Follow the <a href="#generic-upgrade">GENERIC SCRIPT UPGRADE</a></p>
      <p>NOTE: also replace the following files:</p>
      <ul>
        <li>template/footer.php</li>
        <li>template/navbar.php</li>
      </ul>
      <p>or simply change the following functions inside these files:</p>
Old version:
<pre>
&lt;?php echo getString('title').' &copy; '.date('Y'); ?>
&lt;?php echo langMenu('menu'); ?>
</pre>
New version:
<pre>
&lt;?php echo qrcdr()->getString('title').' &copy; '.date('Y'); ?>
&lt;?php echo qrcdr()->langMenu('menu'); ?>
</pre>

      <p>Updated options inside the config.php file:
        <pre>
'rounded_buttons' => '["tabnav", "options", "save"]',   // selective Rounded buttons: '["tabnav", "options", "save"]',
'debug_mode' => false,                                  // set true to track errors,
'precision' => 'H',                                     // available: L, M, Q, H
        </pre>
      </p>
  </div>

  <div class="col-md-12 py-4">
    <div class="alert alert-success">
    <h2 id="generic-upgrade">GENERIC SCRIPT UPGRADE (valid from any version)</h2>
    <p>1) Backup all the files, then replace everything except for:</p>
    <ul>
      <li>/qrcodes/ (folder)</li>
      <li>/template/ (folder)</li>
    </ul>
    <ul>
      <li>config.php (file)</li>
    </ul>
    <p>2) Check to have all the options inside the file config.php (sometimes new options are added)</p>
    </div>
  </div>

</div>
      <hr>

      <h2>Log History</h2>
<pre>
Version 5.2.9
- Fix: load available logo (raised in v.5.2.8)

Version 5.2.8
- New: Privacy policy modal popup
- New: Terms and conditions modal popup
- New: custom pages
- Update: Security patch

Version 5.2.7
- Update: support unicode chars inside frame label
- Update: New Chinese font
- Fix: Safari bug downloading png without logo or background image
- Fix: xlink:href to support pdf export with embedded images

Version 5.2.6
- Update: preloader to save process

Version 5.2.5
- Update: chinese translation
- Update: New markers
- Update: PHP 8 support
- Update: href attribute instead of xlink:href for svg image elements
- Fix: Vcard format name
- Minor css layout fixes


Version 5.2.4
- Fix: frame color with gradient foreground

Version 5.2.3
- New: Background image
- New: Masked background image
- Update: send email in W3C format
- Update: better mobile view for vertical layout
- Fix: black background color

Version 5.2.2
- Update: html_entity_decode frame label text
- Fix: export .pdf with svg icons

Version 5.2.1
- Update: new fonts available
- Update: better frame label text alignment
- Update: handle special chars for frame label text
- New: French translation
- Fix: generate pdf (bug with Chrome)
- Fix: logo position with frame

Version 5.2.0
- New: Resize logo
- New: Custom fonts for frame label text
- New: resize frame label text
- New: download .PDF (available for QR codes without gradient)
- Update: replace bootstrap-colorpicker with Spectrum
- Update: partial support for Bootstrap 5

Version 5.1.7
- Update: PHP 8 support, fix deprecated functions

Version 5.1.6
- New: RTL support for Arabic, Azeri, Dhivehi, Hebrew, Kurdish, Persian (farsi), Urdu
- Update: default front and back colors inside process
- Update: default size inside process
- FIx: vcards name bug

Version 5.1.5
- Update: error correction level optimized, best readability with low precision and logo selected
- Update: validate urls with special chars inside main domain
- Update: optional session_name
- Update: max-length for text areas
- Update: Optimized ajax call
- Update: Toast alerts
- New: Chinese language (thanks to duan2001)
- Fix: Correct Vcard address format also without country field
- Fix: add version to loadQRcdrJS()
- Fix: load multiple custom logos after first upload

Version 5.1.4
- New: deep linking with specific #tab
- New: option relative_path
- Fix: update options after first live preview
- Update: separate sections for colors and size options
- Update: hexdec conversion for php >= 7

Version 5.1.3
- Fix: get current language inside process
- Fix: avoid double click on save button

Version 5.1.2
- Update: support for IE 10 & IE 11, drop support for IE < 10
- Update: refresh live preview after 3 sec.
- Update: validate urls without protocol
- Update: check PHP version >= 5.4
- Fix: Update PayPal main currency and shipping currency

Version 5.1.1
- Update: 1 new frame
- Update: check if XLS extension is enabled
- Update: UTF-8 encoded Vcard address
- Update: default precision option inside config file

Version 5.1.0
- New: Live Qr-code preview
- New: Default OpenMaps if no GoogleMaps API provided
- Update: 1 new Frame
- Update: Full list of currencies available with PayPal
- Update: selective rounded buttons for Tabnav, Options and Save button
- Update: all functions wrapped inside class
- Update: set session samesite strict for php >= 7.3
- Update: wrap main javascript into a jquery plugin
- Update: debug mode option
- Update: minified scripts
- Fix: support svg images with default logos

Version 5.0.1
- Fix: right margins to frames with complex QRcodes

Version 5.0.0
- New: Advanced patterns
- New: Frames option with custom labels
- New: Different color for each marker option
- New: Sidebar position option
- New: Accordion / toggle settings option
- New: Rounded buttons option
- Update: New markers
- Fix format number for USD / BTC rates

Version 4.0.9
- Update: save .png Android support
- Update: Fax field inside Vcards
- Fix: Vcard phone values

Version 4.0.8
- Update: accept SVG watermarks
- Update: validate special chars inside urls
- FIx: visible SVG PNG button for Qrcode download

Version 4.0.7
- New: Navbar as template file
- Update: better vertical layout pagination
- Fix: remove line breaks from tel countrycodes dropdowns

Version 4.0.6
- Fix: internal server error

Version 4.0.5
- New: Layout option Classic or Vertical
- New: Polish language
- Update: Event reminder, Link and Notes
- Update: Bitcoin price in real time from Coinbase

Version 4.0.4
- New: Event calendar
- New: Zoom reunion
- New: Remove background behind Logo
- Update: Editable Latitude and Longitude fields for location
- Update: Vcard improved
- Update: values 'lat' and 'lng' moved inside the file confg to set the initial map position
- update: new default watermarks
- Fix: Create high resolution .png for Safari browser
- Fix: Display marker on the map opened with Android

Version 4.0.3
- New: Skype Chat and Call
- Update: remove anti-alias from generated .png
- Fix: Switch language
- Fix: Print QRcode

Version 4.0.2
- Fix: pre-process watermark
- Fix: sanitize language variable

Version 4.0.1
- Update: Spanish language
- Update: refresh generated QRcodes

Version 4.0
- New sidebar template
- New: Custom QR-code Eyes (markers)
- New: Gradient colors
- Update: New patterns
- Update: Save only .svg version on server
- Update colorpicker
- Update: client side user logo thumbnails

Version 3.3
- Fix: Encode quotes "" inside text messages

Version 3.2
- Update: Hidden option for the wifi connection

Version 3.1
- New: WhatsApp option
- Update: Verify BitCoin address
- Update: label and description to BitCoin payment

Version 3.0
- New: BitCoin payment link
- New: custom QRcode pattern
- New: visual form validation
- New: set main generator theme color
- Update: header and footer in templates
- Update: more png sizes
- Update: BootStrap 4
- Update: new watermarks
- Fix: vcard fields not accessible on mobile view

Version 2.0
- Update: select V-card version and set utf-8 rencoding

Version 1.9
- New: optional transparent background for generated .png 
- New: transparent support for watermarks 
- Update: set default timezone 
- Update: QR_FIND_BEST_MASK false to keep the same code when we have the same content 
- Update: new bootstrap-colorpicker.js 
- Update: jQuery 3

Version 1.8
- Fix: Google maps api bug</li>

Version 1.7
- New: vCards improved with JobTitle, Website and Fax fields</li>
- Update: API KEY for google maps
- Fix: vCard Company title bug
- documentation update

Version 1.6
- New: starter template page included
- New: optional value "detect_browser_lang" inside config
- Update: function getLang() rewritten
- Update: minor code optimizations
- documentation update

Version 1.5
- Update: Transparency support and highest resolution for watermarks
- Update: Multilanguage Meta description and meta tags

Version 1.4
- New: PayPal checkout tab

Version 1.3
- New: Print button
- Update: Portuguese language added (thanks to RJCS)
- Update: German language added (thanks to Black-Shadow)

Version 1.2
- New: Telephone call tab
- New: Text message field for SMS
- New: Dropdown menu with telephone country codes

Version 1.1
- New: language switcher
- Update: Spanish language added (thanks to Germanoronoz)
- Update: Italian language added
- Fix: programmatically remove also .eps generated files
</pre>
 
        <p>&nbsp;</p>

      </div>
    </div>
  </div>
<script src="https://code.jquery.com/jquery-3.3.1.slim.min.js" integrity="sha384-q8i/X+965DzO0rT7abK41JStQIAqVgRVzpbzo5smXKp4YfRvH+8abtTE1Pi6jizo" crossorigin="anonymous"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.7/umd/popper.min.js" integrity="sha384-UO2eT0CpHqdSJQ6hJty5KVphtPhzWj9WO1clHTMGa3JDZwrnQq4sF86dIHNDz0W1" crossorigin="anonymous"></script>
<script src="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/js/bootstrap.min.js" integrity="sha384-JjSmVgyd0p3pXB1rRibZUAYoIIy6OrQ6VrjIEaFf/nJGzIxFDsf4x0xIM+B07jRM" crossorigin="anonymous"></script>

</body>
</html>
