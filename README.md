## Prompt 1: A scenario where you might prefer to use a tuple instead of a list. Be sure to explain why immutability is beneficial in this context.

Response: Tuples are best used for data that should not be changed — for example, birthdays, location data, or the dimensions of a building.
In the world of blockchain, if you're trying to persist something on-chain, you might want to encapsulate the data in a tuple. Once added to the blockchain, the data cannot be changed.
In these cases, where the data will never change, the immutability of tuples makes them an excellent choice.

## Prompt 2: A scenario where a list would be more appropriate than a tuple. Highlight how the mutability of lists provides an advantage in this situation.

Response: I would probably use lists for storing journal entries in a note-taking application, for example.  
One might want to edit their notes to correct grammar or spelling in an entry, a list makes that easy.  
You can't do that with a tuple since it's an immutable data structure.

## Prompt 3: What are some potential challenges you might face when working with each data structure, and how would you address them?

Response:
**Tuples**  
If I want to edit one of the elements in a tuple, I won't be able to do so because of its immutable nature.

**Lists**  
If I want to prevent someone from editing my dataset stored in a list, it’s much harder to enforce.  
I would need to explicitly implement protection in my code, whereas a tuple provides that protection implicitly.

## Prompt 3: Provide a code block answer and brief explanation of the code choices used to answer the initial discussion prompt. Also, include code snippets or examples if possible to illustrate your points.

```python
# tuple
empire_state_building = (40.7484333, -73.9856556) # (Latitude, Longitude)
# This works best since there is only one empire state building located at that location which is mostlikely never going to change.
```

```python
journal_entries = [
    "January 11: Started the morning with a strong espresso and a clear mind.",
    "January 12: Finally visited the Empire State Building; the view from the top is incredible.",
    "January 13: Spent the afternoon at the library researching local history."
]
journal_entries[1] = "January 12: Spent the morning at the Metropolitan Museum of Art exploring the Egyptian wing."

# This is clearly better for editing entries than using tuples
```
