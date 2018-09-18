The first step is importing the data.  Here you'll pull in some test data and graph the result.

## Task

First lets download the csv with the data we are going to work with:

`curl -o Electric_Production.csv "https://fred.stlouisfed.org/graph/fredgraph.csv?chart_type=line&recession_bars=on&log_scales=&bgcolor=%23e1e9f0&graph_bgcolor=%23ffffff&fo=Open+Sans&ts=12&tts=12&txtcolor=%23444444&show_legend=yes&show_axis_titles=yes&drp=0&cosd=1939-01-01&coed=2018-08-01&height=450&stacking=&range=&mode=fred&id=IPG2211A2N&transformation=lin&nd=1939-01-01&ost=-99999&oet=99999&lsv=&lev=&mma=0&fml=a&fgst=lin&fgsnd=2009-06-01&fq=Monthly&fam=avg&vintage_date=&revision_date=&line_color=%234572a7&line_style=solid&lw=2&scale=left&mark_type=none&mw=2&width=1168"`{{execute}}

Now you've got the data in in a csv, pull it into pandas and check the format.

<pre class="file" data-filename="app.py" data-target="replace">
import pandas as pd
data = pd.read_csv('Electric_Production.csv',index_col=0)
print data.head()
</pre>

Running the program now should display the first few records of the data set
`python app.py`{{execute}} 

Ok, now let's get a visual of what this data looks like.

First update the index to be timestamps, then update the column name:
<pre class="file" data-filename="app.py" data-target="append">
data.index = pd.to_datetime(data.index)
data.columns = ['Energy Production']
</pre>

Install plotly library
`pip install plotly --user`{{execute}} 

Now import the plotly libraries and create an html page for the graph:
<pre class="file" data-filename="app.py" data-target="append">
import plotly.offline as ply
import plotly.graph_objs as go

graphme = [go.Scatter( x=data.index, y=data['Energy Production'] )]

ply.plot({
    "data": graphme,
    "layout": go.Layout(title="Energy Production Jan 1985--Jan 2018")
}, auto_open=True)
</pre>

Run the program to generate the graph:
`python app.py`{{execute}} 

OK, let's view the graph:.

Render port 8000: https://[[HOST_SUBDOMAIN]]-8000-[[KATACODA_HOST]].environments.katacoda.com/temp-plot.html
