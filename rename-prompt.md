You are a naming assistant. Given a list of file paths and minimal context from a static website, suggest a new filename (basename only, same extension) for each file. Rules:
- Lowercase, kebab-case, no spaces. SEO-friendly and human-readable.
- For HTML: use page purpose (e.g. about-us.html, contact.html). Keep index.html as index.html.
- For CSS/JS: use purpose (e.g. main-styles.css, analytics.js).
- For images: use content (e.g. logo-infygate.webp, hero-banner.webp). Use alt/title when provided.
- Return a JSON object: keys = exact original path strings, values = new basename only (e.g. "main.css"). Preserve extension.
- Do not change path prefix (e.g. css/ stays css/ by returning "name.css" not "css/name.css").

Files and context:
[
  {
    "path": "404.html",
    "context": {
      "title": "",
      "first_heading": "404"
    }
  },
  {
    "path": "about.html",
    "context": {
      "title": "LOGIQ | About Us",
      "first_heading": "ABOUT US"
    }
  },
  {
    "path": "automatic-sliding-doors.html",
    "context": {
      "title": "",
      "first_heading": "AUTOMATIC SLIDING DOORS"
    }
  },
  {
    "path": "contactus.html",
    "context": {
      "title": "LOGIQ | CONTACT US | Logiq Embedded Systems India Pvt. Ltd.",
      "first_heading": "CONTACT US"
    }
  },
  {
    "path": "css/05e9758e7ba08a6cb23c7ed8dcbdbc92.css",
    "context": {
      "path": "css/05e9758e7ba08a6cb23c7ed8dcbdbc92.css"
    }
  },
  {
    "path": "css/138575cd4810b87ba229d0ae35cbc7b8.css",
    "context": {
      "path": "css/138575cd4810b87ba229d0ae35cbc7b8.css"
    }
  },
  {
    "path": "css/13ba64f344e993a859439e268e2dc606.css",
    "context": {
      "path": "css/13ba64f344e993a859439e268e2dc606.css"
    }
  },
  {
    "path": "css/559e64bf161e61fa0aca6e864c78191d.css",
    "context": {
      "path": "css/559e64bf161e61fa0aca6e864c78191d.css"
    }
  },
  {
    "path": "css/75396a9826200975e6cf53d28de6e9d5.css",
    "context": {
      "path": "css/75396a9826200975e6cf53d28de6e9d5.css"
    }
  },
  {
    "path": "css/84d4a0216f16f715d9b301db3a8da352.css",
    "context": {
      "path": "css/84d4a0216f16f715d9b301db3a8da352.css"
    }
  },
  {
    "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css",
    "context": {
      "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css"
    }
  },
  {
    "path": "css/a94e20961d30c18d0d09ea5d80b32b94.css",
    "context": {
      "path": "css/a94e20961d30c18d0d09ea5d80b32b94.css"
    }
  },
  {
    "path": "css/internal-styles.css",
    "context": {
      "path": "css/internal-styles.css"
    }
  },
  {
    "path": "downloads.html",
    "context": {
      "title": "",
      "first_heading": "DOWNLOADS"
    }
  },
  {
    "path": "elevators.html",
    "context": {
      "title": "",
      "first_heading": "ELEVATORS"
    }
  },
  {
    "path": "escalators.html",
    "context": {
      "title": "",
      "first_heading": "ESCALATORS"
    }
  },
  {
    "path": "imgs/00be39268f38a6cc77cdffce52965406.webp",
    "context": {
      "refs": [
        {
          "alt": "ABOUT US",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/04147828e3b7f5751e1e6a46e2064c1b.webp",
    "context": {
      "refs": [
        {
          "alt": "LANDING OPERATING PANELS",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/074ac8c0b08dcdad49c25848a948c9b3.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0deed16538d1e43cd543d1515f6aaf2e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/16d19c9e62f9f42f01eff8e133973e43.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/178359c68f1e69df8f6f8a88a09153be.webp",
    "context": {
      "refs": [
        {
          "alt": "IMGCopycopy",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2b766bb6c642af0c2ad1e7ee6f54ca7c.webp",
    "context": {
      "refs": [
        {
          "alt": "ASKW",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/330aead72a07cf53003540c76cce5fd2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3ff58d53bdfc4f51959aff149e0b39bf.webp",
    "context": {
      "refs": [
        {
          "alt": "GRAPHIC DISPLAYS",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4050d7c07406e8890cd129f20667017f.webp",
    "context": {
      "refs": [
        {
          "alt": "PRODUCTS",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/42958cc2ec0fd1514368460ccbe66008.webp",
    "context": {
      "refs": [
        {
          "alt": "AUTOMATIC SLIDING DOORS",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/575da868c3836458ab4f3bfe80f90718.webp",
    "context": {
      "refs": [
        {
          "alt": "Specs",
          "title": ""
        },
        {
          "alt": "Drawings",
          "title": ""
        },
        {
          "alt": "White Papers",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5e3742117c2fa85c02dedf6256342976.webp",
    "context": {
      "refs": [
        {
          "alt": "ASKW",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/66708864ceece77700734d6745ef6182.webp",
    "context": {
      "refs": [
        {
          "alt": "ASKW",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/69a15e8f3517380938e938946f3dffbc.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/71e36e819a6ad529652335eebe783b4e.webp",
    "context": {
      "refs": [
        {
          "alt": "CAR OPERATING PANELS",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/744f2d0a6b66ca65d3a5f444787c4a93.webp",
    "context": {
      "refs": [
        {
          "alt": "IMGCopycopy",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/79107ea4a119301a045ad0855ae1a81c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "ELEVATORS",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7ad6ee3067e69239a4229107e5d63b5b.webp",
    "context": {
      "refs": [
        {
          "alt": "WHY LOGIQ?",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9415b2df98a262a7bd28576a2707ae9f.webp",
    "context": {
      "refs": [
        {
          "alt": "ELEVATOR INFOTAINMENT SYSTEMS",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9fa0c240911438e311422badac530993.webp",
    "context": {
      "refs": [
        {
          "alt": "ESCALATORS",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b17c6fb7771f004ce3a2ac7e2483fb53.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b32586e5c42171954ec74825cf7c3aab.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bd6d0115cf801db76e3eb81e9f0fab9e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c30068aec14d4d0849eea6027a663962.webp",
    "context": {
      "refs": [
        {
          "alt": "BFG",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ca55667e4002ac92f9cf78c122aaf2e2.webp",
    "context": {
      "refs": [
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ca7de985b9772c885d8c831c4d820613.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cc29305c3abc22420aafb72805cb4378.webp",
    "context": {
      "refs": [
        {
          "alt": "AUDIO ANNOUNCEMENT SYSTEMS",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d6b9928e196594615ddf06a7448f0a97.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "We are a Design and Manufacturing Company that takes our work very seriously.",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/deb739eac86a728c06452445a3480d96.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e2b3ddb07904e18d29f9b0424f097268.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e73235be054d3bfc9a8646355005c7e9.webp",
    "context": {
      "refs": [
        {
          "alt": "ASKW",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ef21017a6fc1ae8c33350fc49ca3e905.webp",
    "context": {
      "refs": [
        {
          "alt": "BFG",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "index.html",
    "context": {
      "title": "LOGIQ | ELEVATORS, ESCALATORS, AUTOMATIC SLIDING DOORS",
      "first_heading": "Control Products, Accessories and Fixtures for"
    }
  },
  {
    "path": "js/03b2eaae6007054a68c38e495f894dba.js",
    "context": {
      "path": "js/03b2eaae6007054a68c38e495f894dba.js"
    }
  },
  {
    "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js",
    "context": {
      "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js"
    }
  },
  {
    "path": "js/0c46896987137b0016246f6bc2243099.js",
    "context": {
      "path": "js/0c46896987137b0016246f6bc2243099.js"
    }
  },
  {
    "path": "js/165d7b0ddfa33362140feea997351b77.js",
    "context": {
      "path": "js/165d7b0ddfa33362140feea997351b77.js"
    }
  },
  {
    "path": "js/16df9ef05001a1741857bf99f5a5738f.js",
    "context": {
      "path": "js/16df9ef05001a1741857bf99f5a5738f.js"
    }
  },
  {
    "path": "js/2a85c11e395a8380b5915443e926b569.js",
    "context": {
      "path": "js/2a85c11e395a8380b5915443e926b569.js"
    }
  },
  {
    "path": "js/34be5330971fdbd18985525bd994b0aa.js",
    "context": {
      "path": "js/34be5330971fdbd18985525bd994b0aa.js"
    }
  },
  {
    "path": "js/35c5f9e096d4da33d2a62031daf14248.js",
    "context": {
      "path": "js/35c5f9e096d4da33d2a62031daf14248.js"
    }
  },
  {
    "path": "js/3d70953a848219e749fedc2cdb906675.js",
    "context": {
      "path": "js/3d70953a848219e749fedc2cdb906675.js"
    }
  },
  {
    "path": "js/3e940a33e44b65c1c0af8bb80a893530.js",
    "context": {
      "path": "js/3e940a33e44b65c1c0af8bb80a893530.js"
    }
  },
  {
    "path": "js/544d012df7acf9c3f0920f67c9e322b9.js",
    "context": {
      "path": "js/544d012df7acf9c3f0920f67c9e322b9.js"
    }
  },
  {
    "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js",
    "context": {
      "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js"
    }
  },
  {
    "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js",
    "context": {
      "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js"
    }
  },
  {
    "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js",
    "context": {
      "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js"
    }
  },
  {
    "path": "js/7260bab328b0ad74815a5efb377bcc67.js",
    "context": {
      "path": "js/7260bab328b0ad74815a5efb377bcc67.js"
    }
  },
  {
    "path": "js/893de96f1b6da546bd7c814964723eca.js",
    "context": {
      "path": "js/893de96f1b6da546bd7c814964723eca.js"
    }
  },
  {
    "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js",
    "context": {
      "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js"
    }
  },
  {
    "path": "js/9455859483e31e4da0e28f10d0742c2a.js",
    "context": {
      "path": "js/9455859483e31e4da0e28f10d0742c2a.js"
    }
  },
  {
    "path": "js/9db10375d298678e53777a2347b87073.js",
    "context": {
      "path": "js/9db10375d298678e53777a2347b87073.js"
    }
  },
  {
    "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js",
    "context": {
      "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js"
    }
  },
  {
    "path": "js/a2261649751fa61b606222c9b2ea3b80.js",
    "context": {
      "path": "js/a2261649751fa61b606222c9b2ea3b80.js"
    }
  },
  {
    "path": "js/b0bade6d42c2702ca85774296cc507c4.js",
    "context": {
      "path": "js/b0bade6d42c2702ca85774296cc507c4.js"
    }
  },
  {
    "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js",
    "context": {
      "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js"
    }
  },
  {
    "path": "js/cecb447a04bbe3e8982190dd6e697120.js",
    "context": {
      "path": "js/cecb447a04bbe3e8982190dd6e697120.js"
    }
  },
  {
    "path": "js/d80b370d82680fc786dcc943a327b9f2.js",
    "context": {
      "path": "js/d80b370d82680fc786dcc943a327b9f2.js"
    }
  },
  {
    "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js",
    "context": {
      "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js"
    }
  },
  {
    "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js",
    "context": {
      "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js"
    }
  },
  {
    "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js",
    "context": {
      "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js"
    }
  },
  {
    "path": "js/faf9ce4e848522206b5c3043551fb2d7.js",
    "context": {
      "path": "js/faf9ce4e848522206b5c3043551fb2d7.js"
    }
  },
  {
    "path": "products.html",
    "context": {
      "title": "LOGIQ | Products",
      "first_heading": "PRODUCTS"
    }
  },
  {
    "path": "support.html",
    "context": {
      "title": "",
      "first_heading": "WELCOME TO LOGIQ SUPPORT"
    }
  },
  {
    "path": "why-logiq.html",
    "context": {
      "title": "LOGIQ | Why Logiq",
      "first_heading": "WHY US ?"
    }
  }
]

Return only a JSON object mapping each path to its new basename (same extension). No other text.