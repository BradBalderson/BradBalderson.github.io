---
layout: post
title:  "Increasing Publication Output with the Paper Skeleton Strategy"
date:   2019-09-28 17:40:34 +1000
---

**The Paper Skeleton Strategy**

**Key Idea: _Define the project in terms of the paper._**

In science the key indicator of research productivity is publications. This objective can make it difficult to strike the right balance between exploratory research and directed research which can be told as a concise story. This is especially the case in Bioinformatics, where projects may not have clear hypotheses at the outset and instead we set out to solve a particular problem. 

One technique which can be employed to help improve publication output is to define the paper we would like to write before commencing the project. This solution is similar to the software engineering approach of Test Driven Development (TDD). TDD involves writing the necessary tests for whether our code is functioning before the actual code is written. Analogously, we can define the success of our project by a clear paper outline, or _paper skeleton,_ at the outset of the project. 

This strategy allows for deficiencies in the project to be revealed early on. Furthermore, writing is an invaluable tool for organising and facilitating the generation of new ideas. It therefore makes sense to create a skeleton of the publication at the beginning, which will constantly be added to and updated as the project develops. This paper skeleton will have the format of headings and dot points highlighting the key arguments and flow.

 

The results should be the most detailed in the paper skeleton, therefore providing the aims in order to complete the project. Subsequently, you continue to add to the results section as you complete the work. As ideas develop while completing the work, you add these points to the relevant sections of the paper skeleton. That way, by the time the results section is finished, when you go to write the other sections you don’t need to be creative in one sitting when you write the paper. Instead, you sit-down and fill out the different dot-points.

 

Further, by having a logical structure at the outset, it will be clear exactly what evidence you will need to complete the paper, which can also be considered a completion of the project. In other words, you define the project in terms of the paper, instead of doing a project and then writing a paper about it! 

With this strategy it directs the research in a way that makes your thoughts as logical as possible and ordered in a way that decreases the initial inertia of writing the paper associated with the project.

 

 Additional Benefits/extensions:



*   Shareable project outlines with collaborators that make the final structure of the project as explicit as possible (therefore more detailed feedback from others).
*   Could track changes to the project outline with git, or even create different branches as the project might extend into different directions.
*   Link the git version with a google doc, that way multiple people involved in the project can add to the outline easily, and all the changes/branch points still tracked with git.

 

 The paper skeleton strategy is algorithmic and can be summarised with the following pseudocode:

 


<table>
  <tr>
   <td><code>from CriticalThinking import generatePaperSkeleton, complete, \          </code>
<p>
<code>                             addToResultsSection, getNewStrategy, \</code>
<p>
<code>                             updatePaperSkeleton, completePaper \
  \
def getPaper(current_idea):</code>
<p>
<code>    """Creates a paper skeleton from an initial idea and \</code>
<p>
<code>       subsequently utilizes this to complete the project \ </code>
<p>
<code>       and return the completed paper. \
  \
       Args: \
           current_idea (Thought): The initial idea behind the project. \
  \
       Returns: \
           (str): The final paper indicating a successfully completed project. \
                  Will return None if current_idea is not feasible. \
    """ \
  \
    #generating initial paper skeleton and queue of the results to complete \
    paper_skeleton, results_state = generatePaperSkeleton(current_idea) \
  \
    #while there are still parts of the results section to fill out \
    while len(results_state) != 0: \
        todo = results_state.pop() \
        result, result_state = complete(todo) \
                                	 \
        #result worked out favourably \
        if result_state == 'SUCCESS': \
            paper_skeleton = addToResultsSection(result, paper_skeleton) \
  \
        #result didn't work out how you'd expect \
        else: \
            current_idea = getNewStrategy(result, current_idea) \
            if str(current_idea) == "Unfeasible": \
                return \
                                          </code>
<p>
<code>            #update paper_skeleton based on new idea of project \
            paper_skeleton, results_state = updatePaperSkeleton(paper_skeleton, \
     	                                                           current_idea) \
  \
    #fill out the paper skeleton with actual writing \
    paper = completePaper(paper_skeleton) \
    return paper</code>
   </td>
  </tr>
  <tr>
   <td>
   </td>
  </tr>
</table>



<!-- Docs to Markdown version 1.0β17 -->

