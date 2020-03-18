# specs

## Redundant Objects fusion

When redundant, 2 objects may be fusionned : one will keep all properties and the second one deleted. If properties are in conflict, a choice is proposed. A possibility of fusion cancellation is proposed.

### PERS

Other object pointing towards the second one will point towards the first one

## Access rights

### PERS
`private ::Boolean` If true, only the owner can access this person. Modifications are traced and can be cancelled.

`owner ::id` : ID of the owner of the person. Modifications are traced and can be cancelled.

`viewer [::id]` : List of the IDs of the person that can view this private person. Modifications are traced and can be cancelled.

`delegate [::id]` : List of the IDs of the person that can modify this private person. Modifications are traced and can be cancelled.

To manage the rights : you can apply rules (that will be applied automatically and that you can change and reapply)

- rules on all objects : 
	- set/unset (private, viewer, delegate) on all persons.
- rules related to specific objects :
	- set/unset (private, viewer, delegate) on ascendant of X,
	- set/unset (private, viewer, delegate) on ascendant and then descendant of the ascendants of X,
	- set/unset (private, viewer, delegate) on descendant of X,
	- set/unset (private, viewer, delegate) for X.
- automatic rules for setting private : 
	- person born after DATE,
	- person married after DATE,
	- person dead after DATE

Specific display : 
- a key icon will appear for private persons
- a template will display the information on viewer and delegates 

A filter should be available to find the persons according to their access righta

### LIEU 

- public to everybody, but modifications are traced
- management of LIEU types : ex : moulins ?
- management of LIEU like la grande/petite/haute/martinière : group to be made and phonetical search


### DOC

`private::Boolean` property

`owner ::id` : ID of the owner of the person. Modifications are traced and can be cancelled.

`viewer [::id]` : List of the IDs of the person that can view this private person. Modifications are traced and can be cancelled.

`delegate [::id]` : List of the IDs of the person that can modify this private person. Modifications are traced and can be cancelled.

To manage the rights : you can apply rules (that will be applied automatically and that you can change and reapply)

- rules on all objects : 
	- set/unset (private, viewer, delegate) on all docs.
- rules related to specific objects :
	- set/unset (private, viewer, delegate) for doc X.
- automatic rules for setting private : 
	- doc after DATE.

A filter should be available to find the docs according to their access righta

### HIST

public to everybody, but modifications are traced


## Publications

"private" object are published only to there owner, delegates or viewers.

If the person is not published, the template will display "private person" or "private document" (with specific icon).

## Modifications traced

How to do it ?

## GEDCOM import

To be done


## UI

- popup for all data modification (maybe except textXML in line if it is not possible to have a movable popup)
- do not route if popup opened
- Fullscreen possibility for sub templates

## Make multi objects vievers
Can display a list of objects to be displayed :
ex : - multiple docs displayed and choose the want you want to see, edit. Make it possible to have full screen on the in-edition doc .
