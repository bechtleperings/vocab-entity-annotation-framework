# Journey

Recommendations should reflect previously visited content. 


Attentation in language models refers to a technique, which regards the previous dialogue to further tune the future outcome. 

A recommendation is typically not isolated, but is offered within a specific context. Take the following use cases as example: 

- Susan is looking for a new sleeping bag for her kid. She goes through the search results in an online shop and ignores most of the recommdations, because they are irrelevant for her (too warm, too expensive, not organic, etc.). She reads the details of a few products, but the recommendations don't reflect her browsing history and are not updated accordingly. 
- Kevin is checking is favorite channels on a streaming platform. He spends  some time watching videos about downhill bike racing. The recommendations still suggest to watch videos he has just see a couple of minutes ago. Any new recommendations divert and suggest videos about bike shopping or car racing. 
- Justin is preparing a presentation for school about the irish famine. He found an interesting website ...


Keywords
- Ant Colony Algorithm
  - Recommendation Paths, feedback as pheromones (optimal paths for each learning goal)
- Each feedback should ideally include some correlation id representing the whole journeyl



## Example

```turtle
@prefix eav: <http://w3id.org/eav/> . 

:x a sdo:LearningResource
  sdo:requiresCompetency esco:SkillA

<<:x sdo:requiresCompetency esco:SkillA>> 
  eav:recommendation :r1
  eav:recommendation :r2

:r1 a eav:Recommendation
  eav:confirmCount 42
  eav:rejectCount  12
  eav:positiveFeedback "good recommendation"

:r2 a eav:Recommendation
  eav:confirmCount 3
  eav:rejectCount  45
  

```

<!---
issue: 
 recommendations are part of the graph, not dynamically computed


-->

