---
title: 'Life'
date: 2026-11-03
type: landing

design:
  spacing: '4rem'

sections:
  # ── Travel: one entry per destination, newest first ──
  # To add a destination:
  #   1. put its photos in a new folder, e.g. assets/media/life/kyoto/
  #   2. copy a whole `- name:` entry below (down to its last photo) and fill it in
  # Mix scenery and food photos freely; leave `image: ''` to show an "Add a photo" tile.
  - block: travel-journal
    id: travel
    content:
      title: Travel
      text: Heat flows from hot to cold. I flow from the lab to the road.
      destinations:
        - name: '[Destination]'
          date: '[Month Year]'
          emoji: 🏔️
          # TODO(Jia): where was this, and what was memorable (the hike, the view, the food)?
          text: '[A few lines about the trip: the trail, the view, the best thing you ate.]'
          photos:
            - image: life/above-the-clouds.jpg
              caption: '[Above the clouds · where?]'
            - image: ''
              caption: '[Scenery]'
            - image: ''
              caption: '[Food]'

        - name: '[Next destination]'
          date: '[Month Year]'
          emoji: 🍜
          text: '[A few lines about it.]'
          photos:
            - image: ''
              caption: '[Scenery]'
            - image: ''
              caption: '[Food]'

  # ── Music ──
  - block: beyond-lab
    id: music
    content:
      title: Music
      # TODO(Jia): fill in, or delete any card you don't need
      text: '[One line about music and you]'
      items:
        - emoji: 🎧
          title: On repeat
          text: '[Song - Artist]'
        - emoji: 🎼
          title: Favourite artists
          text: '[Artists or genres you love]'
        - emoji: 🎹
          title: '[I play / A concert I loved]'
          text: '[An instrument you play, or a live show that stayed with you]'
      # Optional playlist player. Paste the embed URL from Spotify (Share > Embed playlist) or
      # NetEase Cloud Music (生成外链播放器), e.g.
      #   embed: https://open.spotify.com/embed/playlist/<ID>
      #   embed: https://music.163.com/outchain/player?type=0&id=<ID>&auto=0&height=430
      embed: ''
      embed_height: 380

  # ── Notes: diary-style reflections (content/post/) ──
  # To write a note, copy content/post/note-template/ to a new folder and follow the steps inside.
  - block: notes-list
    id: notes
    content:
      title: Notes
      text: Reflections on Ph.D. life, research and the road.
      count: 3
      placeholder: '[First note coming soon.]'

  - block: markdown
    content:
      title: A few fun facts
      text: |-
        - 🧮 I came to heat transfer through mathematics: my undergraduate degree was in *Information and Computational Science*.
        - 🌡️ [A fun fact about you]
        - 🗺️ [One line about life in Hong Kong]
        - ☕ [Coffee or tea?]

        *Say hi on [Instagram](https://www.instagram.com/jialiu00) or [X](https://x.com/jia_liu00).*
    design:
      columns: '1'
---
