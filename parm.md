# ParM Cheat Sheet

ParM is a presentation framework that helps in managing and organizing slides effectively. Here is a cheat sheet with the most useful ParM commands and features.

## Basic Commands

### Create a New Presentation
```sh
parm new <presentation-name>
```

### Open an Existing Presentation
```sh
parm open <presentation-name>
```

### List Presentations
```sh
parm list
```

### Delete a Presentation
```sh
parm delete <presentation-name>
```

## Slide Management

### Add a New Slide
```sh
parm slide add <slide-title>
```

### List All Slides
```sh
parm slide list
```

### Delete a Slide
```sh
parm slide delete <slide-number>
```

### Move a Slide
```sh
parm slide move <slide-number> <new-position>
```

### Edit Slide Content
```sh
parm slide edit <slide-number>
```

## Slide Navigation

### Go to Next Slide
```sh
parm next
```

### Go to Previous Slide
```sh
parm previous
```

### Go to a Specific Slide
```sh
parm goto <slide-number>
```

## Presentation Modes

### Start Presentation
```sh
parm start
```

### Stop Presentation
```sh
parm stop
```

### Pause Presentation
```sh
parm pause
```

### Resume Presentation
```sh
parm resume
```

## Themes and Styles

### List Available Themes
```sh
parm theme list
```

### Apply a Theme
```sh
parm theme apply <theme-name>
```

### Customize Theme
```sh
parm theme customize
```

### Reset to Default Theme
```sh
parm theme reset
```

## Export and Import

### Export Presentation to PDF
```sh
parm export pdf <filename>
```

### Export Presentation to HTML
```sh
parm export html <filename>
```

### Import Slides from Markdown
```sh
parm import markdown <file-path>
```

## Configuration

### Set Default Theme
```sh
parm config set default-theme <theme-name>
```

### Set Presentation Title
```sh
parm config set title <presentation-title>
```

### Set Author Name
```sh
parm config set author <author-name>
```

### View Current Configuration
```sh
parm config view
```

### Reset Configuration
```sh
parm config reset
```

## Advanced Commands

### Duplicate a Slide
```sh
parm slide duplicate <slide-number>
```

### Merge Presentations
```sh
parm merge <presentation-name1> <presentation-name2>
```

### Split Presentation
```sh
parm split <slide-number>
```

## Tips

- **Using Slide Numbers Efficiently:** Number your slides logically to make navigation easier.
- **Backup Presentations:** Regularly export your presentations to avoid data loss.
- **Utilize Themes:** Applying and customizing themes can significantly enhance the visual appeal of your presentation.