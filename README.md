The Digital Business Card Project
=================================

An effort to evolve the old paper business card into newer social formats as Passbook, HTML5+hCard, VCF.

![two faces of a Passbook pass](https://cloud.githubusercontent.com/assets/3484242/4873626/2b9949d2-621d-11e4-8e2a-f44aafe6faeb.png)

The QRcode on the Passbook pass points to an URL on your website (mine is https://Avi.Alkalay.net/card/) that intelligently
delivers your digital business card as a pass or visual and mobile-friendly HTML5+hCard with links to the pass and VCF.
All with good-looking design and nice icons.

The whole idea is to avoid paper business cards in an easy and work-environment-acceptable way. The journey is:

1. I show my business card in Passbook format on my smartphone.
2. The other person scans the code with iPhone-native Passbook app (or with Android third party Passbook app, see below) and get my card from my website as a pass into his Passbook app.
3. Non-Passbook users can scan the same code and get pointed to a mobile-friendly page on my website that visually resembles a phone contact.
4. There are visual icons to help the user to download my VCF file and, again, the Passbook pass.

The rendered page shows your personal data as e-mail and phone. But it is safe from e-mail
crawlers because the HTML is just a template that is mixed with the actual data using
JavaScript on the visitor's browser. There is no server-side engine, no PHP, no MariaDB
and nothing dynamic is required on the web server side. All are plain static files.

Usage
=====

1. For the HTML page with your digital business card, edit the data.json file with your data.
2. Put your square photo on photo.jpg file. 
3. Test it all by simply viewing the index.html file on you browser. No web server is required for testing.
4. Upload the following files to your web server:
  1. .htaccess (contains logic for passbook delivery and mime-types definitions)
  2. resources (the entire directory with icons and images)
  3. index.html
  4. photo.jpg (your photo)
  5. data.json
  6. vcard.vcf (your business card as a VCF file, supported by all address book software)
  7. passbook.pkpass (your business card as a Passbook pass)
  8. passbookscreenshot.png (to make your URL look nice when sharing on Facebook)
5. Make it all available in a nice URL on your web site. Mine is https://Avi.Alkalay.net/card/

You can get a vcard.vcf file creating a contact of yourself on your smartphone and then sending it to you attached on an e-mail.
Dettach it, rename it to vcard.vcf and upload it with the rest of your files.

Passbook
========

A Passbook pass is not required but is what actually makes the exchange of digital business cards fun, relevant, fast, colourful and effective. People will not forget you.

My Passbook source code is included here as a reference and for my control. You can only make a Passbook pass that will be accepted by
iOS devices if you digitally sign it with an Apple certificate that you can get if you are a paying Apple iOS developer (US$99/year).

If you aren't, I can sign one for you if you send me a Bitcoin donation, minimum B$0.03. This is what you need to do:

1. Edit passbook/pass.json, passbook/en.lproj/pass.strings, passbook/LANGUAGE.lproj/pass.strings with your data.
2. Carefuly chose and put your Digital Business Card URL on the passbook/pass.json file for the QRcode.
3. This URL has to be HTTPS, otherwise the Passbook app will not accept the card. You can get a free SSL certificate (HTTPS) for your site on https://StartSSL.com.
4. If you don't have an HTTPS server and if you convince me you are a good person, I can host your passbook for you in some URL as https://Avi.Alkalay.net/.cards/your-card.pkpass. Not perfect but users don't actually see it. More B$0.09 please, for your lazyness of not making a free HTTPS server for yourself.
5. Put your photo, thumbnail and company logo on top of what you find on passbook folder.
6. You can freely add and remove fields on your Passbook. Also make it active editing fields as your birthday, your geolocation, iBeacons etc. You can see examples on my template.
7. Zip the passbook folder and send it to me with the Bitcoin donation.

I'll send you back a valid (tested) Passbook pass with my digital signature for you to give to your contacts as your new business card.

Passbook on Android and Windows Mobile
======================================

I heard Windows Mobile now supports Passbook passes natively. Android user can install third party Passbook apps such as these:

https://play.google.com/store/apps/details?id=com.sec.android.wallet
https://play.google.com/store/apps/details?id=com.google.android.apps.walletnfcrel
https://play.google.com/store/apps/details?id=tw.com.freedi.passbook
https://play.google.com/store/apps/details?id=com.attidomobile.passwallet

```
Your friend,
Avi Alkalay <avi at unix do sh>
2014-11-01
Made in Brazil
```