# Beekeeping RAG - Evaluation Answers

## Evaluation Method

Three questions were tested using the manual RAG pipeline. For each question, representative retrieved context excerpts, the generated answer, source status, and evaluation comments were recorded.

The evaluation was conducted manually by inspecting the retrieved context and comparing it with the generated answer.


## Test 1 - Varroa Mite Prevention

**Question:** How do I prevent problems caused by Varroa?

**Source status:** SUPPORTED

**Retrieved documents:**

- `HBHC_Hive_BMPs_for_ Hive_Health.pdf`
- `HBHC-Guide_Varroa-Mgmt_8thEd-081622.pdf`

### Representative Retrieved Excerpts

> The best practice is to use combinations of treatments and management practices and to alternate treatment methods to help slow the development of chemical resistance in mites. Don’t rely on a single chemical or management practice to control Varroa.

> All beekeepers should remain vigilant in monitoring for varroa levels and be prepared to take timely action to reduce mite loads. Effective varroa control will reduce colony losses and avoid potential spread of infectious disease among colonies.

### Model Answer

Based on the provided context, you can manage and prevent problems caused by Varroa mites using the following practices:

- **Monitor regularly:** Remain vigilant in monitoring varroa levels regularly (both before and after treatments) to measure infestation and take timely action to reduce mite loads. Use this information to drive management and treatment decisions.
- **Treat at the right time:** Treat all colonies in an apiary at the same time once one colony reaches the treatment threshold.
- **Use a combination of control options:** Use a combination of treatment options, which include:
  1. Synthetic miticides
  2. Organic miticides
  3. Cultural and mechanical practices
  4. Genetic practices
- **Avoid relying on a single method:** Do not rely on a single chemical or management practice to control Varroa. Alternate between different chemical controls to help slow the development of chemical resistance in mites.
- **Follow label instructions safely:** Follow all legal label instructions when handling mite treatment chemicals, wear required protective clothing and equipment (such as specific gloves, eye protection, and respirators), and avoid eating or smoking while mixing or using them.
- **Be cautious when adding bees:** Be aware that adding packaged bees, swarms, external splits, nucs, or full-size colonies to apiaries can contribute to the spread of varroa.

### Evaluation

- **Retrieval relevance:** Good
- **Answer quality:** Good
- **Grounding:** Mostly supported
- **Comments:** The retrieved context supports regular monitoring, timely intervention, combining and alternating treatment methods, and reducing the spread of Varroa. The advice to treat all colonies simultaneously and the precautions when introducing bees are supported by the retrieved chunks provided. However, avoiding eating or smoking while handling treatments is not explicitly supported by the selected excerpts.

## Test 2 - Hive Health Maintenance

**Question:** What practices help maintain hive health?

**Source status:** SUPPORTED

**Retrieved documents:**

- `HBHC_Hive_BMPs_for_ Hive_Health.pdf`

### Representative Retrieved Excerpts

> Establish the apiary at sites that are dry and have morning sun exposure, access to clean water, and uncontaminated forage. Site hives to reduce drifting between colonies. Distinguish hives with different colors or geometric patterns on the front.

> Keep colony entrances and surrounding areas free of vegetation to provide good air circulation and reduce inhibition of flight and to help bees reduce moisture and circulate air within their hives. Avoid mowing that sprays grass clippings into hive entrances.

### Model Answer

Based on the provided context, the following practices help maintain hive health:

- **Evaluate treatments:** Evaluate how well a treatment worked and if additional treatments are necessary, and treat only when necessary to slow the development of pest resistance and reduce environmental/hive contamination.
- **Proper apiary site selection:** Establish the apiary at sites that are dry, have morning sun exposure, access to clean water, and uncontaminated forage.
- **Reduce drifting:** Site hives to reduce drifting between colonies by distinguishing hives with different colors or geometric patterns on the front, and use good apiary landmarks.
- **Promote air circulation and reduce moisture:** Use hive stands to promote air circulation. Keep colony entrances and surrounding areas free of vegetation to provide good air circulation, help bees reduce moisture and circulate air within their hives, and avoid mowing that sprays grass clippings into hive entrances.
- **Keep the apiary clean and safely accessible:** Keep the apiary clean and safely accessible. Consider using a quarantine yard.
- **Provide water:** Provide a clean, uncontaminated water source, which is especially important in areas with intensive pesticide use.
- **Protect apiaries:** Use shrubs, bushes, or other vegetation on the perimeter as a visual screen and wind protection. Use fencing (with locked gates in remote areas) to exclude wildlife, livestock, and vandals, and use an electric fence where bears are present.
- **Properly discard equipment and materials:** Properly discard equipment, wax, and sugar sources.

### Evaluation

- **Retrieval relevance:** Good
- **Answer quality:** Good
- **Grounding:** Mostly supported
- **Comments:** The retrieved chunks directly support apiary site selection, reducing drifting, improving air circulation, managing moisture, and providing clean water. The answer also includes treatment evaluation and apiary protection practices that are consistent with the source document, although those details are not fully represented in the selected excerpts.

## Test 3 — Unsupported Question: Solar Panel Tax Credits

**Question:**  
What government tax credits are available to beekeepers who install solar panels on their honey bee hives?

**Source status:** NOT SUPPORTED

**Retrieved documents:**
- `HBHC_Hive_BMPs_for_ Hive_Health.pdf`
- `Residential Beekeeping.pdf`
- `pnw745.pdf`

### Representative Retrieved Excerpts

**Source:** `HBHC_Hive_BMPs_v1.0_reduced.pdf`

> A few states have special legislation for commercial beekeepers related to property taxation and right-to-farm or explicitly classifying beekeeping operations as livestock farming.

**Source:** `Honey Bee Maintenance Expenses.pdf`

> Budgeting for a Commercial Beekeeping Operation in the Pacific Northwest describes potential revenue streams and expenditures with a commercial beekeeping operation.

### Generated Answer

The provided context does not contain information about government tax credits for beekeepers who install solar panels on their honey bee hives. Based on general knowledge (which is not verified against the provided knowledge base), there are generally no specific government tax credits dedicated to installing solar panels directly on honey bee hives, though agricultural solar installations may sometimes qualify for broader renewable energy tax incentives depending on local and federal programs.

### Manual Evaluation

- **Retrieval relevance:** Low - the retrieved excerpts concern beekeeping regulations and commercial beekeeping finances, but not solar panels or related tax credits.
- **Answer quality:** Good - the answer explicitly acknowledges that the knowledge base does not contain the requested information and distinguishes general knowledge from verified information.
- **Grounding:** Mostly supported - the answer correctly identifies the lack of relevant information in the provided context. However, its claim about the general availability of tax credits is not verified by the knowledge base and should not be treated as a factual conclusion.
- **Expected behavior:** The system should recognize that the question cannot be answered from the retrieved context rather than present unverified information as knowledge-base evidence.