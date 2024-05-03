---
header:
  - type: typewriter
    methods:
      - typeString: Hello world!
      - pauseFor: 2500
      - deleteAll: true
      - typeString: Strings can be removed
      - pauseFor: 2500
      - deleteChars: 7
      - typeString: <strong>altered!</strong>
      - pauseFor: 2500
    options:
      loop: true
      autoStart: false
    height: 190
    paddingX: 50
    align: center
    fontSize: 44
    fontColor: yellow

  - type: text
    height: 200
    paddingX: 50
    paddingY: 0
    align: center
    title:
      - "Everest"
    subtitle:
      - "The roof of the world."
    titleColor:
    titleShadow: true
    titleFontSize: 44
    subtitleColor:
    subtitleCursive: true
    subtitleFontSize: 18
    spaceBetweenTitleSubtitle: 16

  - type: img
    imageSrc: images/header/bg1.jpg
    imageSize: cover
    imageRepeat: no-repeat
    imagePosition: center
    height: 235
    paddingX: 50
    paddingY: 0
    align: center
    title:
      -
    subtitle:
      -
    titleColor:
    titleShadow: false
    titleFontSize: 44
    subtitleColor:
    subtitleCursive: false
    subtitleFontSize: 16
    spaceBetweenTitleSubtitle: 20

  - type: slide
    height: 250
    options:
        startSlide: 0
        auto: 5000
        draggable: true
        autoRestart: true
        continuous: true
        disableScroll: true
        stopPropagation: true
    slide:
      - paddingX: 50
        paddingY: 0
        align: center # left, center, right
        imageSrc: images/header/bg3.jpg
        imageSize: cover
        imageRepeat: no-repeat
        imagePosition: center
        title:
          -
        subtitle:
          -
        titleFontSize: 44
        subtitleFontSize: 16
        spaceBetweenTitleSubtitle: 20

      - paddingX: 50
        paddingY: 0
        align: center
        imageSrc: images/header/bg4.jpg
        imageSize: cover
        imageRepeat: no-repeat
        imagePosition: center
        title:
          -
        subtitle:
          -
        titleFontSize: 44
        subtitleFontSize: 16
        spaceBetweenTitleSubtitle: 20

      - paddingX: 50
        paddingY: 0
        align: center
        imageSrc: images/header/bg5.jpg
        imageSize: cover
        imageRepeat: no-repeat
        imagePosition: center
        title:
          -
        subtitle:
          -
        titleFontSize: 44
        subtitleFontSize: 16
        spaceBetweenTitleSubtitle: 20
---
