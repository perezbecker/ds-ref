# Setting up

Change default browser, to allow interactive authentication with Azure ML 

`sudo update-alternatives --config x-www-browser`


```bash
There are 2 choices for the alternative x-www-browser 
(providing /usr/bin/x-www-browser).

  Selection    Path                       Priority   Status
------------------------------------------------------------
* 0            /usr/bin/chromium-browser   40        auto mode
  1            /usr/bin/chromium-browser   40        manual mode
  2            /usr/bin/wslview            30        manual mode

Press <enter> to keep the current choice[*], or type selection number: 2
update-alternatives: using /usr/bin/wslview to provide 
/usr/bin/x-www-browser (x-www-browser) in manual mode
```

```python
import test

```