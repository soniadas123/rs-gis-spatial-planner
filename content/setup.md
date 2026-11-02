# Getting Started

All notebooks run in **Google Colab**, a free service from Google that runs Python in your web browser.
All you need is a Google account.

## Opening a notebook

1. Go to any lesson page and click the **Open in Colab** button.
2. The notebook opens in a new browser tab.
3. If Colab asks you to sign in, use your Google account.

## Running the code

A notebook is made of **cells**. There are two kinds:

- **Text cells** explain what is happening. Read these.
- **Code cells** have a grey background and a play button on the left.

To run a code cell, click the play button, or click inside the cell and press `Shift + Enter`.
Run the cells **in order, from top to bottom**. Each cell builds on the ones above it.

!!! tip "Run everything at once"
    The menu option **Runtime > Run all** runs every cell in order. This is handy if you only want to see the results.

## The first cell installs packages

Each notebook starts with a cell like this:

```python
!pip install osmnx leafmap
```

This installs the extra tools the notebook needs. It takes about a minute, and you can ignore the long text it prints.
If Colab shows a warning about restarting the session, click **Restart session**, then carry on from the next cell.

## Warnings in red

You may see messages in red or pink boxes that say `Warning`. These are usually harmless notes from the software.
An actual problem says `Error` and stops the cell from running.

## Saving your work

Colab does not save your changes to the original notebook. To keep your own version:

- **File > Save a copy in Drive** saves it to your Google Drive.

## When something goes wrong

- **A cell fails with `NameError`.** You probably skipped a cell. Run the cells above it first.
- **Downloads are slow or time out.** The data servers can be busy. Wait a minute and run the cell again.
- **OpenStreetMap downloads fail with `502`, `504` or `Read timed out`.** Lessons 1 to 5 and 10 download OSM data from the
  public Overpass server, which is sometimes overloaded. Wait a few minutes and try again, or switch to a mirror server
  by running this line after the imports:
  `ox.settings.overpass_url = "https://overpass.kumi.systems/api"`
- **Everything is stuck.** Use **Runtime > Restart session**, then **Runtime > Run all**.

## Changing the study area

Every notebook uses Bengaluru, but you can switch to your own city. Look for the settings cell near the top:

```python
CITY = "Bengaluru, Karnataka, India"
```

Change the name or the coordinates to your own city and run the notebook again. Some ward data only exists for Bengaluru,
and the notebooks point out where that is the case.
