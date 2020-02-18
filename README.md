# specs

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

public to everybody, but modifications are traced

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
