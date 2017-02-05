# SequelPro Bundles

I decided these should be saved somewhere, despite how basic and easy to redo they are.

## Requirements

- php 5.4+ (sorry, used [] array syntax)

## Install

On OSX, your SequelPro bundles are stored in `~/Library/Application\ Support/Sequel\ Pro/Bundles`.

SequelPro will auto-detect anything valid that gets moved into there.

You merely need to copy the directories from this repo, to that dir.

The directories of this repo are there only to organize and indicate what each type of bundle is.

```
export BUNDLE_DIR=~/Library/Application\ Support/Sequel\ Pro/Bundles;

cp -r data_table/input/JSON\ Array.spBundle $BUNDLE_DIR;

cp -r input/format/Apply\ Visible\ Whitespace_Copy.spBundle $BUNDLE_DIR;

# ... continue for whichever interest you
```

Now, when you select rows in the `Content` and right click, you will find `Bundles -> Copy -> JSON Array`.

And, when you select text in the `Query` view, you can right click and `Bundles -> Format -> Apply Visible Whitespace`.

There are no assigned keyboard shortcuts, so if you want them, edit in Bundle Editor.

## Explained

```
├── data_table
│   └── copy
│       ├── CSV          -- Copy as CSV (because SequelPro's Copy does TSV)
│       ├── JSON Array   -- Copy as JSON object literals, wrapped in an array
│       ├── JSON Objects -- Copy as JSON object literals, one per line (not wrapped in array)
│       └── PHP Array    -- Copy output of var_export() array of arrays
└── input
    └── format
        ├── Apply Visible Whitespace -- Any visible \n, \t, \r will be replace with their normally invisible char codes.
        └── Strip Visible Whitespace -- Any visible \n, \t, \r will be replaced with a space (so two words don't get combined into one).
```
