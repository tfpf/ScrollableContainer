# Scrollable Frame for Tkinter
If you have developed GUI applications, you probably know the pain of designing a clean front-end only to find that
your application window is too large for your client's screen. Making the content scrollable is not straightforward, at
least in Tkinter. Especially not after you have already written a lot of code to draw the content.

You can use `ScrollableFrame` to reduce headaches. Check the `main` function in
[`ScrollableFrame.py`](ScrollableFrame.py) to see how.

## TL;DR
Add widgets to the `frame` attribute of a `ScrollableFrame` object.
```python
import tkinter as tk

from ScrollableFrame import *

root = tk.Tk()
scrollable_frame = ScrollableFrame(root)
for _ in range(100):
    tk.Label(scrollable_frame.frame, text='Label').pack()
scrollable_frame.pack(expand=True, fill=tk.BOTH)
root.mainloop()
```
