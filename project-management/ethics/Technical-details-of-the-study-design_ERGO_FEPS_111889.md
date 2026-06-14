# Technical details of study design
## WP1: Landscape mapping
This work package serves as a pilot test of our landscape mapping methodology, designed primarily to evaluate the appropriateness of the data structure and the effectiveness of the relational mapping process. The goal is to validate the technical workflow before any formal analytical conclusions are drawn from the landscape, likely in a separately funded project.

### Data Architecture and Lifecycle Management
The project uses a structured pipeline to move from participant input to a relational database, governed by strict privacy controls.

- **Ingestion**: Data is captured via Microsoft Forms, providing a standardised entry point for all participants.
- **Enforced normalization**: The form uses closed-loop selection (drop-downs/multi-select) rather than open-text entries. These selections are synchronized with SharePoint Lookup Columns, to ensure consistency of element references.
- **Relational storage**: Data is managed within a custom Microsoft SharePoint Lists environment, so individual items can be updated without breaking links between them.
- **Sensitive fields**: The data contain identifiable data (for example names, affiliations, see DPA for full list of variables) but excludes Special Category data.
- **Consent Logic**: A specific "Public Display Consent" field is used as a hard filter. Only records with affirmative consent are pushed to the external visualization.

### Data Processing
The relational lists are exported from SharePoint into CSVs. A custom script is then used to transform the data structure and relationship into the required structure for Kumu. For the public map, a transformation script (or filtered view) automatically strips non-consented rows and contact-sensitive columns.

### Network Modelling 
The mapping follows a multimodal relational architecture, designed to visualise the connections between elements.

#### Node Taxonomy
- Primary Nodes (Actors): Individual participants.
- Secondary Nodes (Anchors): Institutional employers and professional research communities.

#### Edge logic
Edges are categorized by their relational directionality:
- Membership Edges: Linking individuals to their respective communities and employers.
- Organizational Edges: Linking Communities directly to Institutions where a formal hosting or funding relationship exists.

This multi-layered approach will enable the rapid identification of not only who is active in the field, but which organizations provide the structural scaffolding for that activity.

### Visual Analytics via Kumu
The project utilizes Kumu’s visualisation engine to position elements in the visualisation. Kumu’s physics-based settings cluster stakeholders around shared affiliations, revealing the density of support within specific communities. Elements are colour-coded by "Sector" (e.g., Government vs. Academia) to identify cross-sector collaboration.

Node size will be specified in advance to show proportional differences between elements (form smallest to largest: people, communities and institutions). Users can select any node to view its associated metadata, for example a community’s domain of activity or a web profile. Users of the maps can search across all metadata fields to locate specific nodes or criteria. Filters will also be constructed to show topics of interest, for example all communities which have people responsible for communications activity.

### Privacy by Design: Tiered Visualization
To balance utility with privacy, the project generates two distinct outputs from the SharePoint backend:

<table>
<colgroup>
<col style="width: 15%" />
<col style="width: 40%" />
<col style="width: 43%" />
</colgroup>
<thead>
<tr>
<th><strong>Feature</strong></th>
<th><strong>(1) Internal Map</strong></th>
<th><strong>(2) Public-Facing Map</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Data Scope</strong></td>
<td>Full participant dataset (identifiable).</td>
<td>Public consent-only participants.</td>
</tr>
<tr>
<td><strong>Contact Info</strong></td>
<td>Full professional details for internal use.</td>
<td><strong>Excluded.</strong> No email or direct contact.</td>
</tr>
<tr>
<td><strong>Links</strong></td>
<td>Internal records/profiles.</td>
<td>Public professional profiles (e.g., LinkedIn).</td>
</tr>
<tr>
<td><strong>Access</strong></td>
<td>Restricted to project team.</td>
<td>Open access.</td>
</tr>
</tbody>
</table>

## WP2: Qualitative interviews
### Sampling strategy
We are employing a case study approach to achieve our research aim of exploring the scope, value, and impact of Research Community Management (RCM) work undertaken by Research Technical Professionals (RTPs) within the UK research ecosystem, particularly where this work is informal and unrecognised.

We will use a maximum variation sampling method and ensure the diversity of the sample by assessing saturation at different sampling stages. We will begin with purposive sampling to select participants with relevant experiences for the study. These participants will be drawn from the Software Sustainability Fellows cohort and will have indicated they would like to be interviewed during our stakeholder mapping exercise. We will select individuals based on our exclusion criteria and also to ensure a diversity of sample - career stage, type of community, type of organisation and sector. Saturation will be assessed once we have conducted roughly half our interviews, and subsequent sampling will be guided by our stakeholder mapping to ensure sufficient diversity in the study.

### Case selection
We aim to collect diverse and influential cases, those that demonstrate the breadth of community work in the SSI Fellows community. We will document both positive and challenging experiences to enable a more comprehensive analysis. Below is an overview of our inclusion and exclusion criteria.

<table>
<colgroup>
<col style="width: 32%" />
<col style="width: 32%" />
<col style="width: 35%" />
</colgroup>
<thead>
<tr>
<th><strong>Case</strong></th>
<th><strong>Included</strong></th>
<th><strong>Excluded</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td>Role of individual</td>
<td>Any digital Research Professional (dRTP) Role</td>
<td>None dRTP roles</td>
</tr>
<tr>
<td>Type of community role</td>
<td><p>Formal community role - named as Research Community Manager or
variation of this title</p>
<p>Informal community role - not named RCM role but has leadership or
responsibility for delivery of a community activity or task in a dRTP
community or research community of practice</p></td>
<td><p>Does not have formal RCM role or any informal community role</p>
<p>Community participation only</p></td>
</tr>
<tr>
<td>Type of organisation</td>
<td>Research or research related organisation</td>
<td>Non-research organisation</td>
</tr>
<tr>
<td>Geographic location</td>
<td>UK</td>
<td>Non-UK</td>
</tr>
<tr>
<td>Sector</td>
<td>All sectors included</td>
<td>None</td>
</tr>
<tr>
<td>Career stage</td>
<td>Early career research professionals onwards</td>
<td>Undergraduates or below</td>
</tr>
</tbody>
</table>

### Data Collection

#### Sources of data
The data collection in our study includes both primary and secondary sources.

- Secondary data: Documentation from individuals, organisations and communities of practice included as case studies, when relevant and accessible.
- Primary data: Original data collected from digital research technical professionals conducting community work who meet our selection criteria.

#### Semi-structured interviews
Data for inductive study will be collected between April 2026 and June 2026 through qualitative interviews.

Interviews, defined as ‘intensive individual conversations with a small number of respondents to explore their perspectives on a particular idea, program, or situation’ (Boyce & Neale, 2006), are especially well-suited to examining new or poorly understood phenomena. They provide detailed insights into the processes underlying observed patterns and offer access to rich, subjective data that captures participants’ experiences, perspectives, and emotions.

This study will draw on a series of semi-structured interviews, one of the most commonly used techniques in qualitative research (DiCicco-Bloom & Crabtree, 2006), working towards a Grounded Theory model of data collection for future investigations (Glaser & Strauss, 1967) In this format, all interviewees are asked a core set of questions, with flexibility to explore emerging themes or seek clarification as needed. Semi-structured interviews are valued for their balance between consistency and adaptability across diverse research contexts.

We are developing one interview protocol, tailored to our research focuses of the scope, value, and impact of Research Community Management (RCM) work. This protocol will first be piloted internally to ensure questions are clearly worded and non-leading.

We have identified 6 core questions, which will be supplemented by context-specific follow-ups. The questions are open-ended, encouraging participants to reflect and elaborate based on their personal experiences and insights. While all interviews will follow the same foundational structure, we will support exploration towards deepening understanding where there is consistency of themes across participants (saturation) or new themes are uncovered (diversification). As themes emerge, the protocol may be refined slightly, resulting in interviews that vary in focus and flow.

Interviews are expected to last between 45 and 60 minutes and will be conducted online via Microsoft Teams. All interviews will be audio-recorded and transcribed verbatim using an AI-powered transcription service. This data will be manually corrected to preserve accuracy. Both the transcript and audio recording will be retained in line with University of Southampton’s Data Management Policy.

Participants will always be required to sign a consent form covering both the recording and the use of their data in this research.

#### Data saturation
As qualitative research does not aim to produce statistically generalisable results, saturation is used as a criterion for discontinuing data collection and/or analysis (Glaser & Strauss, 1967). Saturation is reached when no new insights emerge from the data that contribute to the development or refinement of a category’s properties.

We follow Saunders et al.'s (2018b) definition of inductive thematic saturation, which emphasises the identification of new codes or themes, reaching saturation when no further codes or themes can be identified through continued data collection.

Because this approach focuses more explicitly on saturation at the level of analysis, it suggests that saturation cannot be defined a priori at the research design stage. However, focusing on the emergence (or lack thereof) of codes, rather than their theoretical development, still implies that saturation may be achieved at a relatively early stage (opposite to other models, such as theoretical saturation, where saturation occurs at a higher level of theoretical abstraction).

### Data analysis
We are adopting thematic analysis as outlined by Braun and Clarke (2006), due to its flexibility and capacity to generate a nuanced, in-depth account of qualitative data.

We adopt an inductive approach, beginning with empirical observations from the data and allowing theories to emerge throughout the research process. As such, no hypotheses are formulated in advance. This approach provides us with the flexibility to adjust the direction of the study as insights develop during the course of the analysis.

EK and CGVP will be responsible for analysing the data. We will follow the six-step process of thematic analysis proposed by Naeem et al. (2023), which builds upon Braun and Clarke’s (2006) foundational framework, while maintaining the methodological flexibility characteristic of qualitative inquiry.

Transcription, familiarisation with the data, and selection of quotations: This stage involves transcribing the verbal data, engaging in active and repeated reading of the transcripts, cross-referencing the data, and making preliminary notes on emerging patterns. Early reflections and annotations lay the groundwork for subsequent coding.

Selection of keywords: A close examination of the interview data allows for the identification of key terms and recurring patterns in participants’ experiences, serving as a bridge between raw data and initial codes.

Coding: Selected excerpts from the data are distilled into concise codes, which are short phrases or terms that encapsulate the underlying meaning. Coding serves as an indexing process, clustering similar ideas and expressions across the dataset.

Theme development: Codes are grouped into broader, analytically meaningful categories. This step marks a transition from direct observations in the raw data to more abstract patterns, identifying relationships among codes and aligning them with the research questions.

Conceptualisation through interpretation of keywords, codes, and themes: Emerging themes, codes, and keywords are synthesised to define key concepts and their interconnections. This phase facilitates movement from specific instances to broader interpretations that frame the findings within a conceptual context.

Development of a conceptual model (or report): The final step involves constructing a comprehensive representation of the data, either in the form of a conceptual model or detailed narrative, to address the research questions and articulate the study’s theoretical and/or practical contributions.

We may use Qualitative Data Analysis (QDA) computer software during our thematic analysis process, such as NVivo. While the research team is familiar with this tool, we are also exploring other alternatives, and we will make decisions based on what we deem to be the most appropriate tool to analyse our data.

We will ensure the inclusion of diverse perspectives by collecting data from multiple sources. Primary data will be gathered through interviews with individuals in a range of roles, seniority levels, and across multiple organisations, rather than relying solely on participants from a single role or institution.

We will have multiple researchers analysing the interviews so that each interview is analysed by two people. Analysts will meet regularly to align on emerging themes and the consistent development of codes.

## Positionality statement
This research is part of the Discovering Hidden Community Leaders project, funded by the Discourse flexible fund and jointly delivered by the Universities of Southampton and Manchester, the Software Sustainability Institute and RCM Cooperative in the UK (February to July 2026).

Researchers in this team are three white women and one white man at mid-to-senior career stages and all in formal Research Community Management roles at research organisations or working directly with research organisations. We bring a range of disciplinary perspectives and complementary skills, and share a strong commitment to advancing diversity, equity, and inclusion in scientific research. Our work is shaped by institutional practices that promote open research and collaborative approaches within project teams. We have previously worked on adjacent topics and actively advocate for professionalisation of digital Research Technical Professional roles. Our positionality will likely bias us towards there being explicit benefits of professionalisation/recognition of RCM roles (question 3), and negative effects of a lack of recognition/support.

We will therefore work with awareness of this bias and afford appropriate weight to views which counter our own. With awareness of this bias, we will apply a “bracketing” methodology to isolate incidents where our beliefs guided questions or responses where they were not informed by the data (including emerging themes). We will also actively seek to enrich responses which contradict our own beliefs, to ground disinformatory evidence.

We acknowledge that both the authorship team and the extended project team lack broader representation in terms of gender and ethnicity. We recognise this limitation and the potential for blind spots in our research process and outcomes.

To address this, we seek to engage and actively include more diverse voices in this study from the dRTP community. Pre-registering our study design is part of our broader strategy to increase transparency, invite external feedback, and support research rigour. We aim to make our study as reproducible as possible for qualitative research.

No explicit conflicts of interest have been identified in relation to this research.
