# Plot Many Points on a Map

**Problem:** Plotting thousands of points on a map using Google's v3 Javascript
API causes a sluggish performance or possibly crashing all together.

**Solution:** Using Google's `Fusion Tables` to render the map on Google's
server greatly improves performance. Plus it adds other useful summary and
plotting tools.

**Required Input** Google's Fusion Table can work with either Google
Spreadsheets, or `.CSV` files. For the plotting to work, you must either have
a column named `Location` with the data formated `latitude,longitude` or two
separate columns: `Latitude` and `Longitude`.

Use [stopCrimes.csv](https://drive.google.com/file/d/0B14oGOf8CrCYOE45UkQ2RGhld0U/view?usp=sharing) as an example.

## Instuctions
1. Log into [Google Drive](https://drive.google.com)
1. Click `NEW` > `More` > `Connect more apps`
1. Search for `Fusion Tables`, click `+CONNECT`
1. Click `NEW` > `More` > `Google Fusion Tables`
1. Either click `Choose File` to upload a `.csv` file\*, click `Google Spreadsheet
to import from there, or click `Create empty table` to enter data manually.

\*When I attempted to upload a CSV file I had issues with the upload. I had to upload
the CSV file into Google Spreadsheets and then link it Fusion Tables. 

Once you have your data loaded into Google Fusion Tables you can generate a map
by clicking the red `+` tab and select `add map`. Also, you can generate a
summary or other charts as well.

One limitation of Google Fusion Table mapping is that it will only display the
first 100,000 entries in a table. If your data set is larger than that you
can apply filters to limit to specific entries, or just allow the first 100,000
entries to be plotted.

## Reference:
* [Too Many Markers!](https://developers.google.com/maps/articles/toomanymarkers)
* [Fusion Table Setup](https://developers.google.com/maps/documentation/javascript/fusiontableslayer#fusion_table_setup)
* [Fusion Tables REST API](https://developers.google.com/fusiontables/)
