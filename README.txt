SMELL & AURA — website files
============================

WHAT'S HERE

  index.html              The whole shop. Catalogue, slideshow, cart,
                          WhatsApp checkout. Everything is inside this
                          one file, including the logo.
  404.html                Shown when someone hits a wrong address.
  favicon.ico             Browser tab icon.
  favicon-32.png
  apple-touch-icon.png    Icon when saved to an iPhone home screen.
  android-chrome-192.png  Icons for Android / installable app.
  android-chrome-512.png
  site.webmanifest        Lets phones "install" the shop like an app.
  og-image.jpg            The picture that appears when the link is
                          shared on WhatsApp, Facebook or X.
  robots.txt              Tells search engines they may index the site.
  _headers                Caching and security settings (Netlify and
                          Cloudflare Pages read this; other hosts ignore it).


HOW TO PUT IT ONLINE

  Netlify   Drag this whole folder (or the .zip) onto app.netlify.com/drop
  Cloudflare  Workers & Pages > Create > Upload your static files >
              drag this folder in
  cPanel    File Manager > public_html > upload, then Extract if zipped

  Whichever host: index.html must sit at the TOP LEVEL of the site, not
  inside a subfolder. If you upload the zip, extract it and make sure you
  don't end up with public_html/smellaura-site/index.html.


CHANGING THINGS

  WhatsApp number
    Open index.html in Notepad or TextEdit, search for WHATSAPP.
    Near the top of the script you'll find:

        const WHATSAPP = "233502296356";

    Digits only, country code first, no + and no spaces.

  Prices, names, sizes
    Search for "products" in index.html. Each fragrance looks like:

        {"id":"dior-sauvage-elixir-elixir-100-ml","brand":"Dior",
         "ab":"DIOR","name":"Sauvage Elixir","type":"Elixir",
         "size":"100 ml","who":"him","price":1430,"hue":24,
         "shape":"obelisk","notes":""}

    price   whole cedis, no comma
    who     "him", "her" or "unisex"
    notes   leave empty, or write the scent notes and they will show
            in the product's Details panel

  Featured on the home page
    Search for "featured". Five entries, each an id and a line of copy.

  Social preview
    Once the site is on its real domain, change the two og:image and
    twitter:image lines in index.html from "og-image.jpg" to the full
    address, e.g. https://smellaura.urbanstudioz.com/og-image.jpg —
    WhatsApp previews are more reliable with the full address.


KNOWN LIMITS

  The cart empties if the page is reloaded. Orders are sent through
  WhatsApp, so nothing is lost, but the basket is not remembered.

  Bottle pictures are illustrations, not photographs. Each one takes its
  colour and shape from the brand. Replace them with real photos when
  you have them.

  No payment is taken on the site. Price, delivery and payment are
  agreed on WhatsApp.
