# ModernZ User Options Guide

### Configuration File Location

Create `modernz.conf` in your mpv script-opts directory:

- Linux: `~/.config/mpv/script-opts/`
- Windows: `%APPDATA%/mpv/script-opts/`
- macOS: `~/Library/Application Support/mpv/script-opts/`

## Available Options

### General

| Option         | Value | Description                                              |
| -------------- | ----- | -------------------------------------------------------- |
| idlescreen     | yes   | show mpv logo on idle                                    |
| windowcontrols | auto  | whether to show OSC window controls. `auto`, `yes`, `no` |
| showwindowed   | yes   | show OSC when windowed                                   |
| showfullscreen | yes   | show OSC when fullscreen                                 |
| greenandgrumpy | no    | disable santa hat in December                            |

### Colors

| Option                | Value   | Description                                                              |
| --------------------- | ------- | ------------------------------------------------------------------------ |
| osc_color             | #000000 | accent of the OSC and the title bar                                      |
| window_title_color    | #FFFFFF | color of title in borderless/fullscreen mode                             |
| window_controls_color | #FFFFFF | color of window controls (close, min, max) in borderless/fullscreen mode |
| seekbarfg_color       | #BE4D25 | color of the seekbar progress and handle                                 |
| seekbarbg_color       | #FFFFFF | color of the remaining seekbar                                           |
| vol_bar_match_seek    | no      | match volume bar color with seekbar color? ignores `side_buttons_color`  |
| title_color           | #FFFFFF | color of the title (above seekbar)                                       |
| time_color            | #FFFFFF | color of timestamps (below seekbar)                                      |
| chapter_title_color   | #FFFFFF | color of chapter title next to timestamp (below seekbar)                 |
| side_buttons_color    | #FFFFFF | color of side buttons (audio, sub, playlist, vol, loop, info..etc)       |
| middle_buttons_color  | #FFFFFF | color of middle buttons (skip, jump, chapter...etc)                      |
| playpause_color       | #FFFFFF | color of play/pause button                                               |
| held_element_color    | #999999 | color of an element while held down                                      |
| thumbnailborder_color | #111111 | color of border for thumbnail (with thumbfast)                           |

### Buttons

| Option                     | Value           | Description                                                                                                                                                   |
| -------------------------- | --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| hovereffect                | size,glow,color | list of active button hover effects seperated by comma: glow, size, color. Ex. `hovereffect=glow, size, color`                                                |
| hover_button_size          | 115             | the relative size (%) of a hovered button if the size effect is selected                                                                                      |
| button_glow_amount         | 5               | the amount of glow a hovered button receives if the glow effect is active                                                                                     |
| showplaylist               | no              | show `playlist` button                                                                                                                                        |
| hide_empty_playlist_button | yes             | hides `playlist` button when a playlist does not exist                                                                                                        |
| gray_empty_playlist_button | yes             | grays `playlist` button when no playlist exists                                                                                             |
| showjump                   | yes             | show `jump forward/backward 10 seconds` buttons                                                                                                               |
| showskip                   | no              | show the `skip back/forward (chapter)` buttons                                                                                                                |
| shownextprev               | yes             | show the `next/previous playlist track` buttons                                                                                                               |
| showinfo                   | no              | show the `info (stats)` button                                                                                                                                |
| showloop                   | yes             | show the `loop` button                                                                                                                                        |
| showfullscreen_button      | yes             | show the `fullscreen toggle` button                                                                                                                           |
| showontop                  | yes             | show `window on top (pin)` button                                                                                                                             |
| showscreenshot             | no              | show `screenshot` button                                                                                                                                      |
| screenshot_flag            | subtitles       | flag for the screenshot button. `subtitles` `video` `window` `each-frame` [[details](https://mpv.io/manual/master/#command-interface-screenshot-%3Cflags%3E)] |
| chapter_softrepeat         | yes             | holding chapter skip buttons repeats toggle                                                                                                                   |
| jump_softrepeat            | yes             | holding jump seek buttons repeats toggle                                                                                                                      |
| downloadbutton             | yes             | show download button on web videos (requires yt-dlp and ffmpeg)                                                                                               |
| download_path              | ~~desktop/mpv   | the download path for videos [[paths](https://mpv.io/manual/master/#paths)]                                                                                   |

### Scaling

| Option            | Value | Description                                    |
| ----------------- | ----- | ---------------------------------------------- |
| vidscale          | yes   | whether to scale the controller with the video |
| scalewindowed     | 1.0   | scaling of the controller when windowed        |
| scalefullscreen   | 1.0   | scaling of the controller when fullscreen      |

### Time & Volume

| Option            | Value    | Description                                                                      |
| ----------------- | -------- | ---------------------------------------------------------------------------------|
| unicodeminus      | no       | whether to use the Unicode minus sign character in remaining time                |
| timetotal         | yes      | display total time instead of remaining time?                                    |
| timems            | no       | display timecodes with milliseconds                                              |
| time_format       | dynamic  | dynamic or fixed. dynamic shows MM:SS when possible, fixed always shows HH:MM:SS |
| timefontsize      | 18       | the font size of the time                                                        |
| jumpamount        | 10       | change the jump amount (in seconds by default)                                   |
| jumpiconnumber    | yes      | show different icon when jumpamount is `5`, `10`, or `30`                        |
| jumpmode          | relative | seek mode for jump buttons                                                       |
| volumecontrol     | yes      | whether to show mute button and volume slider                                    |
| volumecontroltype | linear   | use `linear` or `log` (logarithmic) volume scale                                 |

### Seeking

| Option                 | Value | Description                                                                          |
| ---------------------- | ----- | ------------------------------------------------------------------------------------ |
| seekbarkeyframes       | no    | use keyframes when dragging the seekbar                                              |
| seekbarhandlesize      | 0.8   | size ratio of the slider handle, range 0 ~ 1                                         |
| seekrange              | yes   | show seekrange overlay                                                               |
| seekrangealpha         | 150   | transparency of seekranges                                                           |
| livemarkers            | yes   | update seekbar chapter markers on duration change                                    |
| osc_on_seek            | no    | show osc when seeking                                                                |
| mouse_seek_pause       | yes   | should the video pause while seeking with mouse move? (on button hold)               |
| automatickeyframemode  | yes   | set seekbarkeyframes based on video length to prevent laggy scrubbing on long videos |
| automatickeyframelimit | 600   | videos of above this length (in seconds) will have seekbarkeyframes on               |

### UI [elements]

| Option                          | Value            | Description                                                                |
| ------------------------------- | ---------------- | -------------------------------------------------------------------------- |
| showtitle                       | yes              | show title in OSC (above seekbar)                                          |
| showwindowtitle                 | yes              | show window title in borderless/fullscreen mode                            |
| showwindowcontrols              | yes              | show window controls (close, min, max) in borderless/fullscreen            |
| show_chapter_title              | yes              | show chapter title next to timestamp (below seekbar)                       |
| titleBarStrip                   | no               | whether to make the title bar a singular bar instead of a black fade       |
| title                           | `${media-title}` | title above seekbar. `${media-title}` or `${filename}` (can use `/no-ext`) |
| font                            | mpv-osd-symbols  | mpv-osd-symbols = default osc font (or the one set in mpv.conf)            |
| titlefontsize                   | 30               | the font size of the title text (above seekbar)                            |
| chapter_fmt                     | Chapter: %s      | chapter print format for seekbar-hover. `no` to disable                    |
| tooltips_for_disabled_elements  | yes              | enables tooltips for disabled buttons and elements                         |
| tooltip_hints                   | yes              | enables text hints for the information, loop, ontop and screenshot buttons |
| playpause_size                  | 30               | icon size for the play-pause button                                        |
| midbuttons_size                 | 24               | icon size for the middle buttons                                           |
| sidebuttons_size                | 24               | icon size for the side buttons                                             |
| persistentprogress              | no               | always show a small progress line at the bottom of the screen              |
| persistentprogressheight        | 17               | the height of the persistentprogress bar                                   |
| persistentbuffer                | no               | on web videos, show the buffer on the persistent progress line             |

### UI [behavior]

| Option           | Value | Description                                                |
| ---------------- | ----- | ---------------------------------------------------------- |
| showonpause      | yes   | whether to show osc when paused                            |
| keeponpause      | yes   | whether to disable the hide timeout on pause               |
| bottomhover      | yes   | if the osc should only display when hovering at the bottom |
| bottomhover_zone | 160   | height of show/hide zone for bottomhover                   |
| raisesubs        | yes   | whether to raise subtitles above the osc when it's shown   |
| raisesubamount   | 175   | how much subtitles rise when the osc is shown              |
| thumbnailborder  | 2     | the width of the thumbnail border (thumbfast)              |
| OSCfadealpha     | 150   | alpha of the background box for the OSC                    |
| boxalpha         | 75    | alpha of the window title bar                              |
| loopinpause      | yes   | activate looping by right clicking pause                   |
| visibility       | auto  | only used at init to set visibility_mode(...)              |

### UI [time-based]

| Option                        | Value  | Description                                            |
| ----------------------------- | ------ | ------------------------------------------------------ |
| hidetimeout                   | 2000   | duration in ms until OSC hides if no mouse movement    |
| fadeduration                  | 250    | duration of fade out in ms, `0` = no fade              |
| minmousemove                  | 0      | amount of pixels the mouse has to move for OSC to show |
| tick_delay                    | 0.0167 | minimum interval between OSC redraws in seconds        |
| tick_delay_follow_display_fps | no     | use display fps as the minimum interval                |

### Mouse Commands (User Options)

Customize the button function based on mouse actions.

| Type                          | Option                           | Function                                                                                 |
| ----------------------------- | -------------------------------- | ---------------------------------------------------------------------------------------- |
| Seekbar Mode (mouse wheel)    | seekbar_track_wheel_mode         | default: `seek`<br> accepts `seek` or `speed`.<br>`speed` changes playback speed up/down |
| Title (above seekbar)         | title_mbtn_left_command          | `script-binding select/select-playlist; script-message-to modernz osc-hide`                                                               |
|                               | title_mbtn_right_command         | `script-binding stats/display-page-5`                                                                  |
| Playlist Button               | playlist_mbtn_left_command       | `script-binding select/select-playlist; script-message-to modernz osc-hide`              |
|                               | playlist_mbtn_right_command      | `show-text ${playlist} 3000`                                                             |
| Volume Control                | vol_ctrl_mbtn_right_command      | `script-binding select/select-audio-device; script-message-to modernz osc-hide`          |
| Audio Button                  | audio_track_mbtn_left_command    | `script-binding select/select-aid; script-message-to modernz osc-hide`                   |
|                               | audio_track_mbtn_right_command   | `cycle audio`                                                                            |
|                               | audio_track_wheel_down_command   | `cycle audio`                                                                            |
|                               | audio_track_wheel_up_command     | `cycle audio down`                                                                       |
| Subtitle Button               | sub_track_mbtn_left_command      | `script-binding select/select-sid; script-message-to modernz osc-hide`                   |
|                               | sub_track_mbtn_right_command     | `cycle sub`                                                                              |
|                               | sub_track_wheel_down_command     | `cycle sub`                                                                              |
|                               | sub_track_wheel_up_command       | `cycle sub down`                                                                         |
| Chapter Skip Buttons          | chapter_prev_mbtn_left_command   | `no-osd add chapter -1`                                                                  |
|                               | chapter_prev_mbtn_right_command  | `script-binding select/select-chapter; script-message-to modernz osc-hide`               |
|                               | chapter_next_mbtn_left_command   | `no-osd add chapter 1`                                                                   |
|                               | chapter_next_mbtn_right_command  | `script-binding select/select-chapter; script-message-to modernz osc-hide`               |
| Chapter Title (below seekbar) | chapter_title_mbtn_left_command  | `script-binding select/select-chapter; script-message-to modernz osc-hide`               |
|                               | chapter_title_mbtn_right_command | `show-text ${chapter-list} 3000`                                                         |

### Auto Profile

Below is an example of an auto-profile in `mpv.conf` you can use to set any of ModernZ options based on certain conditions, in this case `when window is pinned or fullscreen`.

```ini
[ModernZ-Custom]
    profile-desc=Apply ModernZ options on pin or fullscreen
    profile-cond=ontop and ontop == true or fullscreen
    profile-restore=copy-equal
    script-opts-append=modernz-persistentprogress=yes
    script-opts-append=modernz-seekbarfg_color=#FF0000
    script-opts-append=modernz-bottomhover=no
    #...etc
```

More information about auto profiles available on [mpv's manual](https://mpv.io/manual/master/#conditional-auto-profiles).
