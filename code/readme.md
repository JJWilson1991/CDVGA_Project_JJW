
## ALS Comments

I've put all of my comments on this page. Overall pretty interesting and I really like your use of plotly!

Update this read me with information especially on the specific order of running the processing scripts. I also made some minor spelling corrections as I found them. Also update all the other readme's or remove them. 

### Processing Code

For the processing code, I don't understand immediately which one needs to be ran first, second or third and if it actually matters. A little more explanation in the very beginning on what the original data is that your pulling in would be nice for the different data sets. I don't understand what a hidden data set with months means. Is this the same data set but now with the months added in? Why is it hidden?

#### CDV Processing

For the CDV Processing you used a Rmarkdown file but then put all the comments inside the code sections. For visuals it's easier to read if it's outside the code portion. You also mentioned that you were going to remove the "Case Numbers" column but you never did. In the end the case number column was present, which is fine, but it's classified as a character instead of numeric. Is there a reason to keep it as a character vs numeric?

#### processingscript.R

For the processingscript.R, the path doesn't work for accessing the file. Actually I think this is the original processing script from the template. If so, delete this file. 

#### Second_Data_Process.Rmd

For the Second_Data_Process.Rmd file, your months, day and year are characterized as characters instead of numeric, is this what you wanted for the final CDVGA_months object? There are two year columns (Year2 and CollectionYear), do these match each other/are they redundant?

### Analysis Code

Having at least some kind of roadmap would be nice. 

#### analysisscript.R

I think this is the original analysis script from the template. If so, delete this file. 

#### ExploratoryAnalysis.Rmd

I ran this one first. I ended up getting an error that the function "corrplot" could not be found. I just skipped over that code chuck and ran the rest of it. There were no other problems. 

You say "i forgot to plot age by species wrap.. its pretty uninteresting" but I didn't see that graph. Does this mean that you just didn't do it but are awknowledging that you didn't?

#### Mapping Script

I ran into an issue running the very last segment of the code. 

> DES3 <- DES2 + 
  geom_point(data = GAcitiesspread, aes(x = long, y = lat, size = pop), alpha = 0.5) + 
  geom_text(data = GAcitiesspread, aes(x = long, y = lat, label = name, group = NULL), position = position_jitter(width=0.3,height=0.3)) 
  
This code returned an error that "object 'pop' not found". 

Other than that. No problems and everything worked. 

Below are just comments. 

The GA maps faceted over years is difficult to see the colors with. 
The ploty of p2 is super cool, but is there any way to make it so that the counties don't look so weird with the lines moving every which way?

I don't know if this is possible but for the plotys over time it would be cool to have it retain which county has already showed up. With an slightly transparent fill that doesn't reset after each year, the counties that are more prevalent will become darker with color over time and it would be eaiser to remember the previously positive counties. 

#### Spatial Analysis.Rmd

I don't know what the difference is between the Spatial analysis.rmd file and the .nb.html file is, or if the .nb.html is just an output of the .rmd file. When running the .rmd file, I needed to load 'dyplr' so that the pipe '%>%' would work. But even after loading that I quickly ran into an issue at line 72, where I got an error saying that the makeplot object for mode function wasn't found. I just skipped over this as well, and then everything else worked. 

#### TimeSeries.Rmd

I recieved the error that object 'RGFAge' not found. As everything was based on that I couldn't move on. 

## Document

I would have liked to have seen a more descriptions/analysis of the figures that you made. For instance, stating the conclusions of each individual figure and the key findings. It's kind of just like a list of your exploratory analysis with most of the reasoning/rationale in the code. It's a little informal

> There did not appear to be any clear diff

One of your references "Alison et al 2013" wasn't in the correct format.






Place your various R or Rmd scripts in the appropriate folders.

You can either have fewer large scripts, or multiple scripts that do only specific actions. Those can be R scripts or Rmd files. In either case, document the scripts and what goes on in them so well that someone else (including future you) can easily figure out what is happening.

The scripts should load the appropriate data (e.g. raw or processed), perform actions, and save results (e.g. processed data, figures, computed values) in the appropriate folders. Document somewhere what inputs each script takes and where output is placed. 

If scripts need to be run in a specific order, document this. Either as comments in the script, or in a separate text file such as this. Ideally of course in both locations.


Depending on your specific project, you might want to have further sub-folders.