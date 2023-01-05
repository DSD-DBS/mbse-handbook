# Modeling rules for system analysis

## Overall

### OEN-001 - Use British English
- In order to ensure consistency within the project, British English is to be used at all times.
Refer to the [Cambridge Dictionary](https://dictionary.cambridge.org/) for further information.

### OEN-002 - Store images and/or diagrams centrally
- Images and/or diagrams that are to be used in the descriptions of Capella model elements shall be created and maintained in a centrally accessible platform.

### OEN-003 - Use auto link in text
- Description Links for model elements shall be used in all model element descriptions. If a model element description refers to (another) model element, the name of this model element shall be referret to in form of some Capella link.


### OEN-004 - Avoid abbreviations
The usage of abbreviations should be well considered and should only be used in cases where the abbreviation is standardised.

The use of abbreviations adds ambiguity and is to be avoided unless the context is clear and the 
abbreviation is clearly defined in the project.  
It is common to have an abbreviation with multiple meanings depending on context.   
In the case where there is a single meaning and that abbreviation is defined in the project, it is acceptable to use the abbreviation.   
However, when there are abbreviations that have different meanings, it is a best practice to avoid 
ambiguity by spelling out the abbreviation. 

## Elements

### Structure in operational analysis

Guidance:
Generally speaking, operational entities should be used for organisations, and operational actors should be used for individual job titles or roles. If you are not sure whether a role belongs to an individual or an organisation, use an operational entity but make a note that it might need to be converted to an operational actor once we have checked.

#### OSE-010 - Use operational entity naming rules

- The name is written in Title Case - the first letter of each word is capitalised, words separated by space.
- The name represents an organisational unit and is consistent with harmonised definitions from collaboration projects or with international standards where applicable.
- Where an operational entity is a type of organisation, the name is generic enough to indicate the type and not to point to individual examples of that organisation (example: "Railway Undertaking (tick)", "XYZ Regio (error)")
- Where an operational entity represents one specific organisation, the name is specific to that organisation and expressed first in English and expressed in German if the original name is German (example: "Federal police (Bundespolizei) (tick)")

#### OSE-010 - Use operational actor naming rules

- The name is written in Title Case - the first letter of each word is capitalised, words separated by space.  
- The name is generic and does not refer to any specific business concern or individual person, although it might describe a role or job type to which an individual belongs.
- Operational actors are indivisible. They are at the level where an individual real person, or an individual system, could realise them. If there is any chance that an operational actor could be subdivided into parts, it should be modelled as an operational entity instead.

#### OSE-020 - Define operational entitiy and operational actor description rules

- The description focuses on the features that define it, not on its responsibilities or activities.
- The description is consistent with harmonised definitions from collaboration projects or with international standards where applicable.

#### OSE-040 - Avoid generalisation for operational entities or actors
- Generalisation between operational entities is not permitted.
- Generalisation between operational actors is not permitted.


### Operational capability

Guidance:
Operational capabilities are a bit like use cases, from the point of view of operational entities in the environment making use of each other.

Detailed guidance and explanations can be found in [ARCH.M.040 Method for definition of capabilities](https://rmt.jaas.service.deutschebahn.com/confluence/display/RA/ARCH.M.040+Method+for+definition+of+capabilities)

#### OCX-010 - Use operational capability naming rules

- The name is written in Sentence case - the first letter of the first word in a sentence is capitalised.
- The name of a operational cpability begin with an active verb.
- Avoid verbs such as "manage", "handle" or "process" as they are not specific enough.
    Rationale: The verb should be specific enough to identify a particular effect on one or more entities/actors in the environment. 

#### OCX-020 - Define operational capability description
- The description includes a brief text description that summarises the capability. It should be short and abstract, because the true description of the operational capability will be its operational entity scenario.

#### OCX-030 - Define pre- and post-condition
- At least one defined pre-condition entered into the corresponding field.
- At least one defined post-condition entered into the corresponding field.

Guidance: 
- states of entities/actors AND/OR abstract concepts can be used to define the pre-condition or post-condition
- exchange items can be evaluated as well
- post-condition describes an observable effect on at least one entity or actor in the environment.

### Activity
Guidance and method can be found in tbd.

#### OAV-010 - Use activity naming rules
- The name is written in Sentence case - the first letter of the first word in a sentence is capitalised.
- The name have the form verb-noun.

#### OAV-020 - Define activity description
- All operational activities have a short text description of the transformation performed by this activity on its inputs to produce the outputs.

#### OAV-030 - Define the rith scope
- Operational activities are defined with a scope that is what an operational entity or actor is responsible for.

### Interaction

#### OIN-010 - Use interaction naming rules
- The name is written in Sentence case - the first letter of the first word in a sentence is capitalised.
- The name begin with a verb in 
- The name of the interaction is not the definition of the interaction (for the definition refer to OIN-010) and will be filtered in diagrams. The name may be freely chosen and should give guidance to the modellers about what is expressed by it.
- The name of the interaction starts with a participle (verb).

#### OIN-010 - Use exchange items to descripe the data exchange of an interaction
- Each interaction has at least one exchange item associated to it. These exchange items define the interaction.
    Exception: If no additional content information is added by the data model e.g. level of detail in the operational level, it is ok to not associate any exchange item and give the interaction just a short description.

### Operational process

#### OPR-020 - Use operational process naming rules
- The name is written in the fowlling pattern, if the process is defined under a capability:
  ```
  <operational capability name> (<Sentence case: additional information that descripes the purpose>)
  ```

### operational scenario
#### OES-180 - Use operational scenario naming rules
- The name is written in the fowlling pattern, if the scenario is defined under a capability:
```
<operational capability name> (<Sentence case: additional information that descripes the purpose>)
```

#### OES-190 Define pre- and post-condition

Note: An Exchange Scenario mays represent either a more specific and detailed course of the main success scenario OR a deviation from the main success scenario (e.g. due to incidents). Therefore the pre- and postconditions of the Capability may apply to the Exchange Scenario or not.

If the pre- and post-conditions of the owning capability fully apply to the Exchange Scenario:

- Pre- and postconditions of owning capability will be selected for Exchange Scenario
- Additional pre- and postconditions represent a refinement or more concrete conditions that apply to this specific scenario. 

If the pre- and postconditions of the owning capability do not (fully) apply to the Exchange Scenario:

- Pre- and postconditions of the Exchange Scenario represent which pre- and postconditions of the owning capability are NOT fulfilled
- Additional pre- and postcondition provide specific context for this scenario

### State and Transition

#### OST-010 - Use state naming rules
- State names contain either adjectives, referring to a quality of the owning entity/actor or verbs in the present participle form (-ing) or verbatim copies of states defined externally to Digital Railway Operation (that is, when reusing state definitions from elsewhere, they should be reproduced precisely and not changed).
- The state name is written in Sentence case - the first letter of the first word in a sentence is capitalised, expect words like commonly known abbreviations or standardised terms which have own (externally-defined).

#### OST-040	- Use only states
- Only states are used in the model. Modes are not used.
  Rationale: The behaviour of both elements in the model is identical and the difference in definition, arising from ARCADIA methodology, is somewhat philosophical. Methodology circle recommends standardising on using only states throughout.

### Decision rationales

tbd 

## Viewponts

### General rules

#### GRV-010 - Use diagram naming convention
Each diagram shall be named according to following convention:

```
[<Capella diagram type abbreviation>][<Viewpoint number>] <Subject of view> [<Viewpoint name>]
```

**Capella diagram type abbreviation:** abbreviation indicating the type of the diagram with the following possible values:

- OCB - Operational Capabilities Blank
- COC - Contextual Capability
- OAIB - Operational Activity Interaction Blank
- OPD - Operational Process Description
- OAB - Operational Architecture Blank
- OES - Operational Exchange Scenario
- O.STM - Operational State Machine (Default in Capella [MSN])

**Viewpoint number:** number given to the viewpoint based on ARCH viewpoint number

**Subject of view:** either a ```<model element>``` or ```<free text>```

- ```<model element>```
  - exact name of the model element
  - is used if the viewpoint focuses on a single model element
- ```<free text>```
  - a useful title providing initial information about the contents of the diagram (e.g. set of model elements shown)
  - is used if the viewpoint does not focus on a single model element or for other cases
  - shall be written in sentence case - the first letter of the first word in a sentence is capitalised

Guidance:

if needed also further information like e.g. sequence diagram main success scenario, alternative scenario, etc. can be included

**Viewpoint name:** name given to the viewpoint based on ARCH viewpoint name

Examples:

[OPD][AMOD-029] Perform passenger exchange [Operational bare business process]
[COC][AMOD-137] Perform passenger exchange [Single operational capability context]
[OCB][AMOD-021] Tactical railway operations (regular situations) [Operational capabilities definition]

tbd