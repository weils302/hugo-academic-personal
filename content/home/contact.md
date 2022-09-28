---
# An instance of the Contact widget.
widget: contact

# This file represents a page section.
headless: true

# Order that this section appears on the page.
weight: 130

title: Contact
subtitle:

content:
  # Automatically link email and phone or display as text?
  autolink: true

  # Email form provider
  form:
    provider: netlify
    formspree:
      id:
    netlify:
      # Enable CAPTCHA challenge to reduce spam?
      captcha: true

  # Contact details (edit or remove options as required)
  address:
    street: Gifu University, Yanagido 1-1
    city: Gifu
    region: Gifu Prefecture
    postcode: '〒501-1193'
    country: Japan
  coordinates:
    latitude: 35.46475
    longitude: 136.73949
  contact_links:
    - icon: weixin
      icon_pack: fab
      name: DM Me
      link: 'http://pnglog.com/i/2022/09/28/6333323fe8779.jpg'
    #- icon: video
    #  icon_pack: fas
    #  name: Zoom Me
     # link: 'https://zoom.com'

design:
  columns: '2'
---
