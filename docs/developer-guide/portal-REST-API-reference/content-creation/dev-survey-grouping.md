
# Survey Grouping

Survey grouping is an effective method to manage and structure surveys. It adds a layer of organization by dividing the survey into various sections. This process is initiated by adding a 'SECTION' item type, complementing the 'QUESTION' type.

## The SECTION item type

A 'SECTION' item type is a group of related questions. Here's an example of what a SECTION item looks like:

```json
{
    "id": 21,
    "revision_id": 1,
    "task_id": "uuid1",
    "name": "Section0",
    "contents": {
        "properties": { // not used in v1.0
            "display_logic": [ // not used in v1.0
                {},
                {},
            ]
        }
    },
    "type": "SECTION",
    "sequence": 1
}
```

Now, two types of items can exist in the survey data structure, namely 'SECTION' and 'QUESTION'.

## Survey Data Structure

The primary survey structure holds the overall data, including the title, status, revision ID, ID, and a list of items. In version 0.9.0, only 'QUESTION' type is supported. Here's a look at the general survey structure:

```json
{
    "revisionId": ...,
    "id": ...,
    "title": ...,
    "status": ...,
    "items": [ ITEM0, ITEM1, ITEM2, ITEM3,.... ] 
}
```

With just 'QUESTION' type supported, a single task would have a list of 'QUESTION' items, like this:

```json
"items": [Q ,Q ,Q ,Q ,Q ,Q ,Q ,Q ,Q ,Q ,Q ,Q ]
```

## Grouping in Survey

Now, with the addition of 'SECTION', grouping becomes possible. 'SECTION' and 'QUESTION' can be sequenced together to form sections of the survey:

```json
"items": [S ,Q ,Q ,Q ,Q ,Q ,Q ,Q ,Q ,Q ,Q ,Q , S ,Q ,Q ,Q ,Q ,Q ,Q ,Q ,Q ,Q ,Q ,Q , S ,Q ,Q ,Q ,Q ,Q ,Q ,Q ,Q ,Q ,Q ,Q ]
```

Each 'S' represents a new section beginning, followed by a sequence of questions. Note that if a 'SECTION' is present in the items, it should always be the first item in a sequence. For instance, the following sequence is invalid:

```json
"items": [Q, Q, Q, S ,Q ,Q ,Q ,Q ,Q]
```

## Benefits of this Design

This design strategy is incredibly beneficial for a number of reasons:

1. **Survey Branching**: It allows for survey branching where participants can either jump to a new section or to a new question, facilitating the creation of complex and dynamic survey paths.

2. **Flexibility**: The design supports surveys without a section, providing flexibility to users to create both sectioned and section-less surveys. This means that it can accommodate a variety of survey types and structures, catering to diverse research needs.

By implementing this design strategy, the survey experience can be greatly enhanced, leading to more organized data collection and analysis.