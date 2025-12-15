# Final Score 186/200

## Grading Criteria

* 2 data sources
* "interesting" take on a problem - not rehash of something from class or kaggle
* method of combining datasets
* dealing with missing values and / or imbalance
* transformations and interactions
* variable selection
* overall EDA
* choosing an appropriate technique
* understanding the assumptions of technique
* fitting a model
* evaluating the model
* overall modeling
* information seems accurate
* conclusions make sense given the analysis
* speaking clearly
* well organized story
* presentation style (slides, graphics, etc)
* overall presentation

## Feedback

Overall, this was an excellent project!  I really enjoyed having the three of you in class this semester, hearing your thought processes, and seeing you learn and work together as a group. What a pleasure!

### Problem Setup

* Great positioning of the problem to look for a relationship between music and consumer sentiment.
* Be very careful with the exact language you use, though. You say that you want to understand if the music features "correlate with or predict **changes** in consumer sentiment."  And the work you did addressed a relationship between the aggregate music features in a specific month and the consumer sentiment in that same month. There was no determination of **changes** specifically. To do that, you would have needed to calculate the delta between one month and another in consumer sentiment.  For example:
  * Compute the change in consumer sentiment from the current month to the next month and use that as the dependant variable... "Do the features of the top music this month predict a change in consumer sentiment between this month and next?"
  * Compute the change from the past month... "Do the features of the top music this month align with a change in consumer sentiment from the previous month to this month?"
  * **(-1 point: misalignment between project statement and work)**
* Excellent selection of data sources. The work you went through to identify appropriate data sources, understand what they represent, dig through what's available and not available, get alignment between the "Hot 100" list and the "Spotify" features -- all excellent work.
* Also a good use of the UMSCENT data. It's a widely referenced source for consumer sentiment.
* One think that would have been great, though I didn't explicitly recommend it anywhere, would be to do some research into whether or not this or a related question has been asked.  I don't recall seeing anything about that in your presentation or our conversation.

### Project Structure

* Clear use of methodology!
* Very easy to follow your work most of the way through.
* As you shared during class, you spent quite a while working with different timeseries data splits for model build and evaluation. While the project was well done, there are some ways in which it feels like the focus was more on exercising and demonstrating the breadth of skills from the is class rather than the specific tools that would be best used in this problem given rules of thumb that we discussed in class.  **(-5 points: I believe that thinking and planning a bit more would have saved you some iterations.)**

### Code Quality and Organization

* Overall, very easy to follow code. Cell names and labels were clear. Variable names were easy to understand and usually followed good naming conventions.
* In **TryTrainTestWindows**, there is a lot of repetative code. The split process could have been built as separate functions to iterate through; The code for testing all of your models with the different splits could have been a function that was called for each different split.  **(-5 points: Several ways to cut the amount of repeated code by >75%.)**
* That said, this was a very smart thing to do. Putting all the split scenarios and model types together in a grid with a performance metric was great.
* Writing out conclusions using print() statements rather than Markdown results in a lot of excess code and doesn't add much value. The **Final Summary** cell is a dramatic example. **(-1 point)**

### Presentation

* Beautiful presentation: good use of theme, great combination of text and visuals
* During the presentation, I appreciated switching back and forth with the notebook.
* There were probably a couple more visualizations it would have been good to pull out and annotate in the presentation itself (e.g., Feature Distribution Before & After Transformation)

### Notebook

* Generally a well organized and easy to follow notebook.
* Excellent use of exploratory charts / data viz.

### Conclusions

* Your interpretation of **Energy and Loudness Sentiment** seems to have reversed the structure of the relationship you're evaluating. Rather than noting the curiousity of more intense music predicting less optimistic times, you observed the inverse possibility of less optimistic times leading to more intense music. **(-2 points: reverse interpretation of independent / dependent variables)**
* Regarding **Energy and Loudness**, also remember back to your VIF analysis?  The VIF was close to or greater than 5 for Loudness and Energy, meaning their could be some concern with interpretation of these variables.
* One thing that would have been great to talk about more in your conclusion would be the implications of your new found understanding and models.  **(-5 points: What does one do now that they know this?)** You mention this in the bottom line, but I wanted to hear more on the "so what" topic.
* Overall, your conclusion was very robust. I appreciate your reflection on this final project and how approached it from so many different angles (Potential Future Research, Limits & Caveats, Pedagogical Value).
