# Reviewer A — Independent candidate position
Cutoff: 2026-11-06. Window: 2020-01-01 through cutoff, with expressly named older anatomy sources handled by Reviewer B. This is a three-perspective review, not independent empirical replication. No external research connector was invoked.

## Stage 1: independent position before reciprocal review
**Candidate A:** pursue Layer A only as a conditional hearing-device development program and Layer B as a separately testable, patient-controlled assistive software option; place chronic Layer C on HOLD pending signal-identifiability and route-safety evidence. A flexible peripheral interface could be worth laboratory investigation, but one to two years of calibration cannot create information absent from the recording site. Favor external face/neck EMG as a low-burden comparator before chronic implantation.

**Strongest competing position:** high-quality peripheral myoelectric signals plus improved sequence models may provide useful limited-vocabulary or articulatory communication even without cortical signals. This warrants a prespecified non-implant feasibility experiment. It does not support unrestricted inner-speech decoding or validate the proposed pharyngeal route.

### Scientific corrections and tested contexts
| Source | What was tested | Consequential boundary |
|---|---|---|
| [SCL001] Willett 2023 | Intracortical spikes in one participant with ALS; 62 WPM; 23.8% WER at 125,000 words | Speech attempt in cortex; no peripheral-route inference |
| [SCL002] Metzger 2023 | One participant with brainstem stroke; 253-channel subdural cortical-surface ECoG; median 78 WPM and 25% WER | Correct the prompt's grouping: this is **not** intracortical single-unit recording; silent attempted articulation differs from inner speech |
| [SCL003] Card 2024 | T15 with ALS, four 64-site arrays = 256 electrodes; final five Copy Task sessions 2.5% WER (95% CI 2.0–3.1) | Selected conversation evaluation: 3.7% (3.3–4.3), 925 known-label sentences; do not interchange denominators or use 2.5% as all-life conversation error |
| [SCL004] Wairagkar 2025 | Voice and prosodic synthesis in T15 using the same implanted cortical platform | This is a longitudinal capability extension, not an independent second ALS participant or pharyngeal validation |
| [SCL005] Kunz 2025 | Four cortical-array participants; inner-speech experiments including T15; keyword-based lock proof of concept | Selected cognitive-task leakage is real within study conditions; no generalized claim of all private thoughts or decoding from tonsillar tissue |
| [SCL006] Salomons 2025 | Face/neck surface-EMG electrode-selection pilot, including 14 muscles in one participant | Useful adjacent-domain comparator; not chronic tonsillar ENG or clinical speech restoration |
| [SCL007] Littlejohn 2025 | Cortical-surface streaming voice framework; abstract reports EMG and single-unit generalization | Algorithmic transfer motivates study; methods not fully inspected and chronic anatomical transfer remains unverified |

Links and complete author lists are in A_sources.json. Card Methods and Results were inspected directly in full HTML. Several publisher pages redirected or PMC pages presented CAPTCHA, so indexed passages and author repositories supplied limited access for the other studies; those are recorded rather than called full reads.

The [Metzger author correction of July 4, 2024](https://www.nature.com/articles/s41586-024-07735-z) reports channel-order errors affecting anatomical assignments and maps; the authors state real-time decoding performance and main outcomes were unaffected. Use corrected maps in any anatomical figure. This correction was inspected through publisher-indexed text.

The physical chain is **cortical motor representation → descending drive → peripheral axon/muscle activity → articulatory motion**. Recording a later node captures only the activity expressed at that node. Silent articulation can produce EMG without sound; imagined speech need not produce a useful peripheral signature. A nerve's proximity to a sensor does not guarantee neural selectivity, sufficient spatial resolution, or sentence information. Pharyngeal sensory/autonomic afferents do not automatically carry an articulatory motor command. An implanted submucosal muscle sensor measures implanted EMG; call it ENG only after nerve-selective signal validation. “sEMG” should be reserved for surface EMG.

The single most consequential unresolved empirical limitation is **whether the proposed chronic tonsillar/submucosal site yields stable, intent-specific communication information beyond swallowing, respiratory and movement confounds with useful accuracy across days**. Neither cortical papers nor better model priors resolve that uncertainty.

### Validation that could change Candidate A
Proposed experiments, not established regulatory acceptance criteria:

1. Within-person, time-separated trials of audible speech, silent articulation, imagined speech, listening, rest, swallowing, coughing, chewing and head movement. Simultaneous external EMG, acoustic and motion controls quantify confounding.
2. Split by day and participant before model selection; hold out sentences and vocabulary where relevant. Exclude prompt leakage and temporal train/test overlap. Use language-model-only, shuffled-signal and nuisance-sensor baselines.
3. Report WER with confidence intervals, correct information transfer, false outputs per hour at rest, abort/abstention rates, effort, latency distribution, calibration minutes and channel/impedance drift. Include unassisted, external-EMG and conventional AAC comparators.
4. Freeze decoder before prospective testing; count model abstention as non-delivery and harmful confident errors separately. Do not optimize test data or hide recalibration burden.
5. Longitudinal route-safety, tissue-response, swallowing and airway endpoints belong to B/C's staged preclinical and regulated clinical program. No seven-year reliability claim follows from a seven-year financial support horizon.

## Patient authority and diagnostic integrity — proposed architecture
The hierarchy is a product requirement: safety, consent, mental privacy and diagnostic integrity precede engagement, model confidence and commercial utilization. It is not proof that a prototype meets it.

**Hardware permission broker:** a physically operable, accessible patient control drives a deterministic state machine outside the LLM. OFF gates elective acquisition/processing and transmitter access, empties local pending synthesis queues, revokes local session credentials, invalidates in-flight response identifiers and denies storage/indexing. Cloud cancellation is best effort; data already transmitted cannot be recalled by a switch. Therefore restrict cloud payloads before transmission and enforce session-bound TTL and deletion contracts. Prevent late cloud responses playing after OFF. Only a fresh patient action may arm the elective mode. Essential Layer A hearing must have separate compute/supply protection and remain operational through elective shutdown.

**Least-privilege care interface:** use allowlisted integrity metrics and indication-specific physiological fields. Raw decoded speech, semantic embeddings and conversational memory are prohibited in default telemetry. Patient-selected clinical excerpts require purpose, recipient and expiry. A clinician's programming privilege does not include unilateral access to the patient's inner speech or remote activation of an elective assistant.

**Differential-attribution gate:** machine quality checks must run before any elective AI symptom/triage inference: impedance/channel faults, saturation/dropout, SNR, calibrated acoustic/stimulation state, swallowing/motion contamination, clock drift and recent configuration changes. The gate must distinguish FAIL from UNKNOWN. Otitis/effusion, tinnitus, vestibular symptoms, listening fatigue and neurological change are not conclusively excluded by good electronic telemetry; human assessment remains necessary. An unresolved checklist results in abstention and a neutral “measurement unreliable / clinical review needed” flag, never a psychiatric label. It must not suppress a patient's own report or delay urgent clinical care.

**No autonomous psychiatric diagnoses:** do not convert HRV, vagal proxies, prosody, pauses or decoder errors into asserted anxiety, depression, intent, concentration, psychosis or somatic symptom disorder. “Frequently misinterpret” is not supported by a quantified rate for this nonexistent integrated platform; treat that sentence as a serious prospective hazard, not an established incidence claim. NIST AI 600-1 [SA001, sections 2.2 and 2.7] supports general confabulation/automation-bias risk, including clinical summary harm; it does not prove the specific psychiatric attribution mechanism.

**EMR export:** provenance must travel with each datum: source class (raw/calibrated telemetry, algorithmic proxy with confidence/validation status, patient-edited self-report), device/software/model version, acquisition and processing time, calibration state, artifact flags, transformation history, uncertainty metric and intended use. A confidence score is not truth. Use a patient review/quarantine state before ordinary AI-summary commit, with visible differences between generated and patient-amended text. Preserve original signed versions and append corrections; do not promise deletion of legally retained medical records. Patient amendment rights and clinician record duties require jurisdiction-specific implementation. AHDS FHIR is a transport/service choice, not an automatic immutable audit trail or consent engine.

**Tests:** power loss, RF loss, app crash, compromised cloud, replayed output, stale consent token, remote-reactivation attempt, battery exhaustion and swallowing artifact injections. Required outcome: no new elective output in OFF, no covert context log and continued Layer A service. Independently instrument latency and hearing interruption, rather than accepting model self-report.

Kunz's neural keyword lock [SCL005] achieved 98.75% accuracy in a specific trial. This cannot replace the physical permission broker: learned decoding remains probabilistic, and a mental password itself presupposes neural sensing.

## Cloud/service economics checked by A
Microsoft's September 29, 2026 launch table [ST008] supports US Data Zone short-context GPT-6.1 Sol rates of $2.20 input, $0.11 cache-read, $2.75 cache-write and $11 output per million tokens. These are dated list benchmarks, not a guarantee of future contracted price or clinical suitability.

Text cost is:
`365 × calls/day × (2.20×uncached_input + 0.11×cache_read + 2.75×cache_write + 11×output)/1,000,000`.
At three calls/day, 1,000 uncached input and 465 output tokens/call, no cache, cost is **$8.010 annually**. This is an explicit illustrative workload, not inferred from “three calls/day” alone. Reasoning output, retries, context growth and monitoring may add cost.

The supplied subtotal is exactly **$168.43 = $8 + $0.43 + $10 + $60 + $90**. Excluding the optional voice allowance gives $158.43. Thus “$159–169” is reasonable rounding only if the range means optional voice excluded/included. The adopted $300 floor provides $131.57 above the full itemization; it is a modeling reserve, not proven adequacy. Add $60 third-party licensing and 10% of software revenue separately.

Voice Live documentation [ST009] lists GPT-6.1 Sol in Pro, with model-dependent audio/text billing and additional custom voice training/hosting. The $10 for 500 total minutes means $0.02/minute; the retrieved current price page renders unspecified dollar values, so that allowance is **unverified as an all-in tariff**. Historical June 2025 Pro standard-audio rates [ST011] were $17/M input and $38/M output. Using 10 input tokens/sec and 20 output tokens/sec with 250 minutes each direction yields **$13.95 audio alone** before text and custom hosting. This is a dated sensitivity illustration, not current pricing. If 500 minutes applies to each direction, double it. A dedicated historical custom-voice endpoint at $4.04/hour would be economically material; deployment-specific hosting/pooling must be quoted.

Microsoft's current migration FAQ [ST010] states Azure API for FHIR was deprecated September 30, 2026, with extension requests mentioned. Specify Azure Health Data Services FHIR; avoid claiming that every old endpoint unconditionally ceased on that date.

## Stage 2 / Stage 3
A's completed reciprocal audit is in A_audit_B.md. Science adjudication, including C_audit_A.md, is in A_judgment.md. C's accepted refinement is mandatory: signal-quality PASS never authorizes psychiatric inference or establishes disease exclusion.

