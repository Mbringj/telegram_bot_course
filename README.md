# telegram_bot_course

## Your first Bot, step-by-step
So, *let's get started!* Again, please fire up a Python command line if you want to follow this tutorial.

First, you have to create an `Updater` object. Replace `'TOKEN'` with your Bot's API token.

```python
from telegram.ext import Updater
updater = Updater(token='TOKEN', use_context=True)
```
For quicker access to the `Dispatcher` used by your `Updater`, you can introduce it locally:

```python
dispatcher = updater.dispatcher
```

This is a good time to set up the `logging` module, so you will know when (and why) things don't work as expected:

```python
import logging
logging.basicConfig(format='%(asctime)s - %(name)s - %(levelname)s - %(message)s',
                     level=logging.INFO)
```
