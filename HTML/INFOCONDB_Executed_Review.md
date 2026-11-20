# InfoconDB archival review and RF measurement validation

**Executed review • 20 November 2026 • Archival research and offline analysis**

The supplied task has been executed as a bounded archival review, technical correction audit and independent replay of the supplied software. The strongest result is a reproducible analysis baseline with a traceable conference register. Conference demonstrations and synthetic fixtures do not identify an unknown device or establish the cause of a reported experience.

The compilation required substantive corrections. It conflated related-talk links with authorship, a scheduled presentation with a delivered talk, some proposed methods with completed validation, and product-family specifications with model-specific capabilities. The revised field manual already resolves several shortcomings of the older drafts; the correction register distinguishes those improvements from remaining defects.

## What was examined

The review opened all **44 indexed ShmooCon XIII session abstracts**, audited **24 medical-device conference records** and **24 radio-analysis conference records**, and checked the official sources for **three software projects**, with WaveConverter added through the ShmooCon screen. These are workstream counts, not a sum of unique talks: overlapping sessions are deduplicated in the consolidated register.

The extension screened **149 appearances on 12 presenter profiles**, representing 141 distinct title/date leads. It added 29 relevant abstract-level records, excluded 67 peripheral leads, identified 38 already represented leads, and retained seven unresolved leads. All 11 requested conference-series catalogs were mapped for coverage gaps; their presentation counters are not counts of reviewed talks. The combined register contains **120 unique conference records** after the one core overlap is removed and the 29 additions are included.

The local source corpus contains the task Markdown, four study HTML documents, the supplied analysis ZIP, a reconstructed 28-page presentation, and a 22-page clinical-textbook excerpt. The excerpt is from *Programming Cochlear Implants*, third edition (2026), and contains front matter and chapter 1 printed pages 1–6; the RF/telemetry section listed on printed page 25 is absent. The PDF page counts were checked locally. Their byte counts and SHA-256 values appear in the source inventory. The separately named **PNG.png was not located**, so its described flowchart was not independently inspected. The task text was recovered through the file reader and matched the recorded 55,949-byte length; the other files were downloaded with their retained identities.

The review distinguishes an opened catalog abstract, an opened primary publication or slide deck, an inspected transcript, and a reproduced computation. A working link alone does not mean its media were reviewed. The scope is not a full audiovisual audit of every conference or every presentation in InfoconDB.

## Findings that change the compilation

| Finding | Corrected disposition | Evidence |
|---|---|---|
| Barnaby Jack, Black Hat USA 2013 | Scheduled but not delivered; the organizer left the slot vacant. Do not cite it as a completed demonstration. | [Black Hat memorial](https://blackhat.com/latestintel/07262013-remembering-barnaby-jack.html); B02 |
| Related-talk links | Similarity is not authorship. Correct Jason Gale, Robert Portvliet, Saurabh Harit, Isabel Straw, and Jeremy Miller/Jonathan Fischer assignments. | B18–B23 and individual record URLs |
| DEF CON 33 medical workshop | The 2025 Aguilar/Delifer workshop is *Medical Device Hacking: 201*; *Med Team vs Red Team* is the 2024 title. | B16–B17 |
| Dodge presentation duration and status | A 30-minute program slot differs from the 21:43 YouTube mirror. The inspected automatic transcript describes complete interpretation and reverse telemetry as future work. | ShmooCon primary program; Appendix A timestamp ledger |
| Carrier and return-link evidence | Manufacturer labeling for specified HiRes Ultra/Ultra 3D models supports 49 MHz forward power/data and a separate 10.7 MHz FM return transmitter. Do not generalize every return link as load modulation. | [FDA-hosted labeling](https://www.accessdata.fda.gov/cdrh_docs/pdf/P960058S167D.pdf), PDF pages 8 and 45 |
| Receiver selection | SMArt v5 supports HF through direct sampling below 25 MHz. XTR vendor documents disagree on a 55/65 MHz floor; both exclude 49 MHz. V4 and V4L have different launch dates and tuners. | TA01–TA05; official vendor sources |
| Field and probe assumptions | Inverse-cube decay is a qualified dipole approximation. Receive-only probes can still load a coupled circuit; they are not intrinsically non-interacting. | TA16–TA18 |
| Software provenance | SDR++ 1.3.2 is a mutable nightly; pin the commit and binary hash. URH is archived. A release's existence is separate from local compatibility testing. | TA11–TA15; C tool register |
| Regulatory currency | The FDA guidance dated 3 February 2026 supersedes the June 2025 version cited in the source. Its recommendations are nonbinding; the statutory and regulatory requirements it cites remain distinct. It does not establish a finding about a particular device. | [FDA guidance cover and scope](https://www.fda.gov/media/119933/download) |
| Publication status | Unresolved citation tokens, repository placeholders and an unprovided DOI cannot support a claim of submission readiness or public deposition. | Corpus correction register |

## Evidence model and inference limits

Use two independent labels. **Evidence tier** describes what the claim concerns. **Review status** describes what was actually examined. A verified conference listing does not promote a device claim to a universal physical law.

| Tier | Appropriate use | What it does not establish |
|---|---|---|
| 1 — Established mechanics and verified baseline | Sampling mathematics, declared synthetic fixtures, the measured output of this offline test run, and version-scoped format rules. | Correct operation of an untested receiver or a particular implanted system. |
| 2 — Device or context specific | Named manufacturer labeling, a speaker's reported measurements, and observations of a specified research prototype. | Transfer to another device generation, geometry, firmware, setting or person. |
| 3 — Reported and unverified | Any uncorroborated assertion about device presence, consent, operator identity, neural decoding or causation. | Confirmation from a diagram, a conference title, an RF peak or the software tests here. |

Review-status terms in the registers include **index inspected**, **primary source inspected**, **transcript inspected**, **computed**, **conflicting**, **unavailable**, and **not performed**. Speaker claims remain attributed even when a transcript is accessible. The title “implantable logic analyzer” and the computer-peripheral implant in *Injectyll-HIDe* refer to different systems from biomedical implants.

## Historical anchor and conference transfer

Jeff Dodge's 2017 session is the correct historical anchor. The primary program and abstract concern his own Advanced Bionics HiRes 90K. The archived schedule confirms 13 January 2017, 17:00–17:30. The automatic transcript of a 21:43 mirror was inspected; its technical numbers and terminology need audio/slide corroboration before use as a protocol specification. No original I/Q recording, oscilloscope dataset, decoder source, independently authenticated slide deck or measurement-calibration record was obtained.

The 44-session screen identifies three directly useful sessions: Dodge's CI presentation, Knight/Newlin's radio introduction, and Paul Clark's **WaveConverter**. Seven others offer conditional methods, including offline emulation, parser discipline and DSP in infrared. Seventeen offer peripheral context and seventeen are excluded. Infrared DSP, EEG authentication and computer hardware implants do not establish CI-link measurements.

Across radio conferences, the transferable workflow is to document the receiver and recording, describe bandwidth and timebase, examine time and frequency structure, compare plausible interpretations, and test the decoder against known examples. Methods are extracted from named sources without importing their active-transmission or exploitation steps. Conference panels contribute governance context, not validated engineering specifications.

The full session and presentation registers preserve corrected coauthors. For example, Dominic Spill coauthored the relevant Ossmann work, Marc Newlin alone presented the TROOPERS18 *Lazy-Mode* talk, and Christiane Ruetten and Sergey Bratus must be retained on the corresponding Goodspeed presentations. Scheduled durations are stored separately from available recording runtimes.

## Materials and instrument capability

Receiver suitability must be represented as a configuration: model, tuner, driver, input path, gain and AGC state, sampling mode, device rate, decimation, and file representation. A frequency on a datasheet is not a demonstrated sensitivity or usable bandwidth at that frequency. A public-FM check exercises its documented configuration and cannot qualify every HF path or inductive measurement.

For SMArt v5, separate its tuner path from HF direct sampling. For XTR, preserve the manufacturer's conflicting lower limits rather than silently selecting one. An upconverter requires separate tuner frequency, oscillator offset and reconstructed RF-axis fields; the Ham It Up mixing oscillator is 125 MHz and its display correction is −125 MHz. For SDRplay, ADC resolution depends on sample-rate mode, while API storage width is a separate property. The detailed RSP1B table is supported; the unavailable historical RSPdx datasheet prevents carrying every setting over by analogy.

The historical RIGOL DS1054Z is a **50 MHz** oscilloscope. There is no universal “at least 100 MHz and at least 20 MS/s” rule that qualifies every proposed measurement. Ordinary direct real sampling of a 49 MHz carrier requires a rate above 98 MS/s before engineering margin; an envelope or intentionally bandpass-sampled signal has different requirements. Resolve the actual measurand, filtering, rise time and uncertainty first. At 2.4 MS/s, a 1.1 Mbit/s Manchester half-bit spans only about 1.09 samples, which does not establish accurate edge shape or ringing.

For an ideal circular loop on axis, the finite-geometry field is proportional to **a²/(a²+z²)^(3/2)**. The inverse-cube approximation requires distance large relative to the loop size, as well as the appropriate near-field regime. A millimeter separation cannot automatically be modeled with that asymptote. Probe loading, aperture and orientation belong in any separately authorized engineering protocol. This execution used no receiver, probe or medical device.

## Methods and data provenance

The executed work comprised source review and offline computations. Live-FM acquisition and device-specific acquisition remain unperformed. This separation is substantive: synthetic validation proves selected properties of a program under controlled input, while live measurement introduces analog response, timebase, interference, clipping and acquisition-state uncertainties.

Preserve the capture and its interpretation metadata together. Record sample type, endianness, component order, sample rate, frequency provenance, source category, acquisition configuration and software identifiers. A two-channel WAVE header does not distinguish stereo audio from baseband I/Q. The analysis route must come from documented provenance, not channel count alone. With unknown tuner-frequency provenance, retain an offset axis rather than inventing an absolute RF axis.

The two-file SHA-256 manifest detects changes relative to the recorded digests. It does not authenticate the original metadata, identify the operator, prove when acquisition occurred or prevent a party from replacing the entire set. Logs, preserved originals and authenticated custody records serve different evidentiary purposes.

The replay exposed an additional interpretation limit: the analyzer checks the `center_frequency_source` text lexically; it cannot independently verify that the stated source is true. A nonempty arbitrary label can enable an absolute-frequency axis for synthetic input, although the output still says `NO_LIVE_CAPTURE`. Treat this field as an operator declaration requiring external verification, not proof of provenance. TA26 records this behavior and its control.

For the supplied SigMF fixture, validation checks the versioned schema, core-key set, canonical I-first representation, payload size, SHA-512, sample extent and relevant semantic constraints. A custom QI input accepted by an analyzer is not automatically a conforming core SigMF recording. Optional unknown fields must be handled according to their type; a universal null/UNKNOWN convention can invalidate typed fields. The package records the actual scope of the conformance checks.

## Analysis and numerical interpretation

The independent replay uses complex two-tone fixtures at +50 kHz and −75 kHz, with the second tone's amplitude set 6 dB below the first. It computes a two-sided spectrum using a periodic Hann window of 4,096 samples and a 2,048-sample hop. Welch averaging is performed in linear power before conversion to dB. The window normalization and resulting units must remain explicit; uncalibrated input units are not dBm, field strength or acoustic dB SPL.

| Quantity | Aligned control | Between-bin case |
|---|---:|---:|
| Sample rate | 1,024,000 samples/s | 2,400,000 samples/s |
| FFT length | 4,096 | 4,096 |
| Bin spacing | 250 Hz | 585.9375 Hz |
| Nearest bin to +50 kHz | +50,000 Hz | +49,804.6875 Hz |
| Bin at −75 kHz | −75,000 Hz | −75,000 Hz |
| Periodic Hann ENBW | 1.5 bins | 1.5 bins |
| Predicted second/first peak-bin ratio | −6 dB | −5.3730907234 dB |

At 2.4 MS/s, +50 kHz lies one-third of a bin from its closest FFT center. Direct finite-window summation gives a −0.6269092766 dB peak loss for that tone. The −75 kHz tone is bin centered, so the peak-bin ratio differs from the encoded amplitude ratio by that amount. This explains the difference without changing the stored amplitude or attributing it to hardware.

The earlier supplement's +50,012 Hz and −74,988 Hz outputs cannot be produced by its stated uninterpolated 585.9375 Hz grid. A different estimator could output non-grid values, but it would need a specified algorithm and actual results. They must not be presented as observed output from the supplied raw-bin algorithm.

The off-bin record contains 98,304 complex samples, or 786,432 bytes for float32 I and float32 Q. It spans integer cycles of both tones, permitting a separate whole-record coherent projection. That calculation checks the encoded amplitude ratio independently of the Hann peak-bin estimate. The package reports current measurements, tolerances and archived-output comparisons rather than copying expected numbers as results.

Negative controls challenge sign and scale: swapped I/Q, a 2% sample-rate metadata change, incomplete data, nonfinite samples, invalid metadata, and capture/sidecar mutation. Rejection is expected for malformed input or a failed fixture oracle; a nonzero exit can therefore be a passing negative-control result. Full details appear in the validation report and JSON logs.

## Clinical and research comparators

The manufacturer label is a stronger source for specified commercial link parameters than an AUDITORY mailing-list question. For HiRes Ultra/Ultra 3D, it describes 49 MHz forward transfer, 1.11 Mbit/s OOK/ASK signaling and a 10.7 MHz FM return transmitter. These values apply to the named systems; they neither identify an ambient signal nor define every CI generation.

UmboMic is a mechanical sensing research program; the 2024 and 2026 papers have different measured noise values and experimental series. A totally implantable CI feasibility study concerns a particular investigational system. Intracortical attempted-speech decoding uses recorded cortical activity and participant-specific training. Their physical inputs, units and endpoints must remain distinct from RF spectra. The literature appendix verifies the exact samples, dates and transfer limits.

The February 2026 FDA cybersecurity guidance is the current version identified as of 20 November 2026. Its cover date is 3 February; the agency topic page uses 2 February. The discrepancy is retained. The guidance addresses cybersecurity design and submission documentation, including recommendations for devices that do not require premarket submission. Its nonbinding recommendations are distinct from the statutory and regulatory requirements it cites, including section 524B requirements for applicable cyber devices. This source review does not determine legal compliance in an individual case.

## Corrections and disposition

The source documents are preserved. The package contains a section-level correction register, a corrected research companion, and copies of the two older HTML drafts with only their malformed ShmooCon event link repaired. The filenames and notices identify those copies as **URL corrections only**; their remaining claims are not endorsed by the link repair. The revised field manual and supplement are not silently overwritten.

This is an executed research and software-validation package, not a claim of journal acceptance, editorial review, clinical validation or complete audiovisual coverage. The open gaps are explicit: original historical measurement files and slides, unavailable catalog/media records, exact details in conflicting schedules, the missing PNG, unperformed live capture, and device-specific measurements.

## Assumptions and acceptance gates

The newest uploaded InfoconDB task is treated as the user's intended task. The source compilation is treated as a set of claims to verify. No access to a connected receiver or verified device is assumed. The review date is 20 November 2026; mutable web pages and software channels require future version checks.

| Delivery criterion | Acceptance gate | Disposition |
|---|---|---|
| Traceability | Every substantive correction has a source, source locator or disclosed calculation. | Registers and source inventory supplied; unresolved evidence is marked. |
| Reproducibility | Original kit hash matches; replay logs, environment, numerical output and expected-failure controls are retained. | See actual execution summary below; interpreter differences are disclosed. |
| Coverage and usability | Bounded populations are counted; missing material is explicit; report opens offline; package contents are hashed. | Full 44-session screening, targeted conference audit, profile extension and validated delivery package. |

The refinements improve the source by replacing implied verification with explicit evidence states, separating device models and measurement domains, and turning expected software behavior into independently recorded test results.


## Executed validation results

**27/27 harness checks passed; 0 failed.** These include positive fixture replays, expected-failure controls and original-kit preservation. Separately, **four schema checks/controls passed**: original and regenerated fixture validation, missing-required-field rejection, and undefined-core-key rejection by the strict check. Neither test group constitutes receiver or clinical validation.

The 153,428-byte source ZIP matches SHA-256 `b89c4f2cf2c5f1b9b2f8dfcb77697ec000fe96838d481452e11b3ace7356c9fa`. The actual interpreter was **CPython 3.12.12**, with **NumPy 2.3.5** and **Pillow 13.0.0**. This is a compatibility replay relative to the source's CPython 3.12.14 environment, not an exact interpreter replication. The installed SigMF Python package is 1.14.0; the checked specification/schema is **1.2.6**, a different version identifier.

| Output | Current measured result | Validation |
|---|---:|---|
| Aligned peak-bin ratio | -6.000000007229 dB | Exact bins; 124 averaged frames |
| Between-bin peak-bin ratio | -5.373091329515 dB | 47 averaged frames |
| Between-bin ratio minus prediction | -6.06139348e-07 dB | Within ±0.001 dB regression tolerance |
| Aligned frequency errors | 0 Hz; 0 Hz | Both centers recovered |
| Between-bin frequency errors | −195.3125 Hz; 0 Hz | Correct nearest-bin behavior |
| Full versioned schema and fixture semantics | PASS for original and regenerated fixture | SHA-512, core keys, data length and extent checked |

The published schema accepts additional nested properties. An intentionally undefined `core:hash` example therefore passes that schema alone but fails the additional core-key check. The package makes this distinction explicit rather than equating JSON validation with complete normative conformance.

The full logs and portable audit scripts are in `validation/`. Reproducible malformed control inputs are generated by the harness and are omitted from this delivery. Archived originals and actual result logs are retained.


---

## Appendix A ShmooCon program and historical anchor

# Workstream A — ShmooCon XIII source and program audit

Accessed: 20 November 2026. Scope: the ShmooCon XIII (2017) InfoconDB index, its 44 linked session records, the Jeff Dodge presenter record, and primary/archive corroboration of the focal talk.

## Result and screening boundary

**44 of 44 indexed session abstracts were opened and screened:** 13 on 13 January, 21 on 14 January, and 10 on 15 January 2017. Classification is an editorial relevance assessment for cochlear-implant/NFMI and RF-characterization research: **3 Direct, 7 Methodological, 17 Peripheral, 17 Excluded**. It is exhaustive only for the session records displayed on the accessed index. It is not a review of every ShmooCon activity, every recording, the wider Infocon collection, or all historical literature. Opening and closing remarks appear in the primary schedule/archive but are not among these 44 indexed sessions.

- **Direct:** explicitly addresses the focal CI system or RF capture/analysis.
- **Methodological:** a transferable analysis or validation technique in another system; applicability is conditional.
- **Peripheral:** provenance, policy, organization, or reasoning context without direct measurement evidence.
- **Excluded:** no material method or evidence for the bounded workstream in the indexed abstract.

Source: [InfoconDB ShmooCon XIII index](https://infocondb.org/con/shmoocon/shmoocon-xiii/). Corroborating [primary archived schedule](https://web.archive.org/web/20170118065527/http://shmoocon.org/schedule/). Conference dates and place are 13–15 January 2017, Washington Hilton, Washington, DC, as reported by the index and [recording collection](https://archive.org/details/ShmooCon2017).

## Focal talk: verified historical status

| Field | Finding | Evidence / limit |
|---|---|---|
| Title | Cyborg Self-Hacking: An Examination of Cochlear Implants | [Indexed talk](https://infocondb.org/con/shmoocon/shmoocon-xiii/cyborg-self-hacking-an-examination-of-cochlear-implants), turn759378408view0 |
| Presenter | Jeff Dodge | [Presenter record](https://infocondb.org/presenter/jeff-dodge), turn759378408view1; one talk is listed on that accessed profile |
| Event | ShmooCon XIII, Friday 13 January 2017 | Primary archived schedule |
| Scheduled time | 17:00 to the next 17:30 slot; catalog says 30 minutes | Schedule allocation, not media duration. Local conference clock; no conversion imposed |
| System named in abstract | The speaker's own Advanced Bionics HiRes 90K | [Primary archived speakers page](https://web.archive.org/web/20170118065535/http://shmoocon.org/speakers/), lines 186–190, turn267175322view0 |
| Nature of record | Historical conference presentation about the presenter's own system and investigation | Not a current clinical study, manufacturer protocol specification, or evidence about another individual |
| YouTube mirror runtime | **21:43 (1,303 seconds)** | Browser player observed after the advertisement was skipped; distinct from 30-minute program slot |
| Mirror title/uploader/date | Cyborg Self Hacking - Jeff Dodge; 0xdade; 30 January 2017 | [YouTube mirror](https://www.youtube.com/watch?v=ihcaNoUJ6BU), browser UI inspection on access date |
| Transcript review | Visible automatic transcript read from 00:00 through final 21:36 cue | Not a word-verified transcript or a full audiovisual/slide audit; export failed after the browser tab became unavailable |
| Archive source | ShmooCon 2017 collection credits Shmoo Group / various presenters; added 25 January 2017 | [Archive item](https://archive.org/details/ShmooCon2017), turn468679995view0; archive publication date is 15 January, distinct from talk date |
| Archive media | ShmooCon2017 - Cyborg Self Hacking.mp4, displayed 388.1M; OGV displayed 49.2M | [File listing](https://archive.org/download/ShmooCon2017), turn212104791view0; displayed rounded sizes are not byte checksums |
| Original media verification | Original archive runtime, byte identity, completeness, and hash remain unverified | No archive video downloaded; do not assume mirror is bit-identical or complete |

The primary abstract supports the intended subjects (CI operation, listening experience, stimulation strategies, channel interaction, and his signal investigation). It does not itself establish a carrier frequency, complete frame definition, functional takeover, or generalization to all implants. The visible recording transcript adds a stronger boundary: interpretation and reverse-telemetry work were still described as unfinished or future work near the end.

## Timestamped recording ledger

These are concise paraphrases of **speaker-reported observations in a visible automatic transcript**, not independently reproduced measurements. Times refer to the 21:43 YouTube mirror. Auto-caption errors are evident; exact technical strings and numbers require audio/slide confirmation before specification-level use.

| Mirror time | Reported content | Evidentiary treatment |
|---|---|---|
| 01:13–01:28 | Describes his CI signal investigation as ongoing. | Scope / status |
| 05:53–06:23 | Describes external processing and inductive power/data transfer. | Historical explanation; cross-check manufacturer documentation |
| 14:54–15:25 | RTL-SDR was used to observe the carrier, not recover signal data. | Speaker report; no archived I/Q validated |
| 15:41–17:16 | Describes oscilloscope capture and preliminary bit extraction. | Method history; no reproduction performed |
| 16:43–16:58 | Interprets the waveform as amplitude-modulated and Manchester encoded. | Speaker interpretation; no raw trace verified |
| 17:25–17:55 | Infers 12-bit words; captions report “300” for usual packet size without reliable units. | Do not promote to protocol specification |
| 18:04–18:37 | Mentions a patent not yet incorporated into his decoder. | Patent identifier not recovered from captions |
| 18:53–19:34 | Claims no encryption, while describing near-field constraints and apparent absence of nonvolatile memory. | Device-specific assertions; require corroboration |
| 20:09–20:39 | Lists complete interpretation, a processor, and reverse telemetry as future work. | **Not a completed control demonstration** |
| 21:24–21:36 | Closing statement and question prompt. | Last visible caption cue; not proof of full Q&A coverage |

Recording source: https://www.youtube.com/watch?v=ihcaNoUJ6BU (browser observation; web service retrieval failed, so no successful web citation ref is assigned to its UI facts). The Royal Society's [iHuman report](https://www.royalsociety.org/-/media/policy/projects/ihuman/report-neural-interfaces.pdf), reference 10 on printed page 92 (PDF index 91), independently points to this video. That citation establishes provenance of the pointer, not independent validation of the talk's technical claims. A search snippet dropped the “J” from the video ID; the opened PDF resolves it as **ihcaNoUJ6BU**.

## Original material versus reconstructed exhibits

No separate original slide deck was located in the accessed InfoconDB talk links, archived program, or archive file listing. This is a search result, not proof that no slide deck exists.

- A frame extracted from a verified original/mirror recording must be labeled **recording frame**, with source, timestamp, extraction date, and any crop/annotation disclosed.
- A newly drawn block diagram, waveform schematic, measurement chain, or timeline must be labeled **analyst reconstruction / illustrative exhibit**, with the sources it summarizes.
- Do not label a recreated figure “Jeff Dodge slide,” a schematic “measured waveform,” or a derived trace “original data.” No original I/Q, oscilloscope trace, decoder source, patent identity, or measurement calibration file was retrieved in this workstream.
- Archive licensing is displayed as Attribution–No Derivative Works 3.0, while the YouTube mirror displays a Creative Commons Attribution license. These differ; neither establishes the mirror uploader's authority to relicense the original. This audit links the materials and supplies original summaries; it does not redistribute or edit third-party video/slides.

## URL defect and access log

| Address / issue | Result |
|---|---|
| https://infocondb.org/con/shmoocon/shmoocon-xiii | Opened successfully; redirected to trailing slash |
| https://infocondb.org/con/shmooocon/shmoocon-xiii | Extra “o” in conference path; retrieval failed. Correct canonical path has **shmoocon**, not **shmooocon**. No HTTP 404 claim is made because the tool reported only inaccessible |
| Infocon media directory and linked Cyborg Self Hacking.mp4 | Restricted/not accessible in web retrieval; a local HEAD attempt also failed DNS resolution |
| Current shmoocon.org | Retrieval failed; dated Wayback captures of original schedule and speakers succeeded |
| YouTube via web service | Failed; browser fallback succeeded for mirror metadata and visible transcript |
| Archive item and file listing | Succeeded; media contents and checksums not downloaded |
| Archive files XML | Failed through web retrieval; no metadata duration/hash obtained |
| Original slide deck | Not found in examined records |
| Search coverage | Exact title/name searches in both search systems, primary program links, profile and media links, Royal Society reference chain. Unrelated search results were not used |

## Complete 44-session register

Each URL below was opened individually, and its full indexed abstract and presenter section were screened. Dates/times are catalog metadata, not verification that each session occurred exactly as scheduled. Presenter spellings follow the indexed page, including aliases. The CSV/JSON companions preserve every web reference and screening rationale.

| # | Date / time | Session | Presenter(s) | Class | Reason |
|---:|---|---|---|---|---|
| 1 | 2017-01-13 3:30 p.m. | [U2F Zero: Secure Hardware Design, DIY Mass Production, and Amazon Prime](https://infocondb.org/con/shmoocon/shmoocon-xiii/u2f-zero-secure-hardware-design-diy-mass-production-and-amazon-prime) | Conor Patrick | Peripheral | Secure hardware provisioning context; no CI or RF characterization method is described. |
| 2 | 2017-01-13 4 p.m. | [35 Years of Cyberwar: The Squirrels are Winning](https://infocondb.org/con/shmoocon/shmoocon-xiii/35-years-of-cyberwar-the-squirrels-are-winning) | Cris Thomas / Space Rogue | Peripheral | Alternative-cause comparison can inform evidentiary caution; infrastructure anecdotes do not identify RF sources. |
| 3 | 2017-01-13 4:30 p.m. | [Implantable Logic Analyzers and Unlocking Doors](https://infocondb.org/con/shmoocon/shmoocon-xiii/implantable-logic-analyzers-and-unlocking-doors) | Kenny McElroy / @octosavvi | Excluded | Facility door-access systems; 'implantable' refers to inserted analysis hardware, not evidence of a biomedical implant. |
| 4 | 2017-01-13 5 p.m. | [Cyborg Self-Hacking: An Examination of Cochlear Implants](https://infocondb.org/con/shmoocon/shmoocon-xiii/cyborg-self-hacking-an-examination-of-cochlear-implants) | Jeff Dodge | Direct | The only indexed session explicitly about cochlear implants; abstract identifies the speaker's own HiRes 90K and an attempted signal investigation. |
| 5 | 2017-01-13 5:30 p.m. | [Introducing Jak: Safely Share Sensitive Files via Git](https://infocondb.org/con/shmoocon/shmoocon-xiii/introducing-jak-safely-share-sensitive-files-via-git) | Chris DiLorenzo | Peripheral | Encrypted source-file collaboration context; no CI-link measurement content. |
| 6 | 2017-01-13 6 p.m. | [Can a Drunk Person Authenticate Using Brainwaves? #NotAlcoholicsJustResearchers](https://infocondb.org/con/shmoocon/shmoocon-xiii/can-a-drunk-person-authenticate-using-brainwaves-notalcoholicsjustresearchers) | Peter Muller; Tommy Chin | Peripheral | EEG biometric authentication using a wireless headset; distinct sensing modality and endpoint from a cochlear-implant link. |
| 7 | 2017-01-13 6:30 p.m. | [Seven Things: Frank Zappa, T. Coraghassen Boyle, and Twenty-one Years in Security](https://infocondb.org/con/shmoocon/shmoocon-xiii/seven-things-frank-zappa-t-coraghassen-boyle-and-twenty-one-years-in-security) | Dr. Gary McGraw | Excluded | Security-career keynote; no relevant measurement or interface method in the abstract. |
| 8 | 2017-01-13 8 p.m. | [Firetalk #1: How to Spoil all Movies and Give an Unforgettable Presentation](https://infocondb.org/con/shmoocon/shmoocon-xiii/firetalk-1-how-to-spoil-all-movies-and-give-an-unforgettable-presentation) | Jason Blanchard | Excluded | Presentation/storytelling advice; no RF characterization evidence. |
| 9 | 2017-01-13 8:20 p.m. | [Firetalk #2: Quick and Dirty Emulation of ARM Firmware](https://infocondb.org/con/shmoocon/shmoocon-xiii/firetalk-2-quick-and-dirty-emulation-of-arm-firmware) | Travis Goodspeed | Methodological | Embedded-firmware emulation is a transferable offline analysis method, conditional on legitimately available firmware. |
| 10 | 2017-01-13 8:40 p.m. | [Firetalk #3: NAVRIE Athena - A graph database solution to unify InfoSec data and workflow](https://infocondb.org/con/shmoocon/shmoocon-xiii/firetalk-3-navrie-athena-a-graph-database-solution-to-unify-infosec-data-and-workflow) | Peter Clemenko | Peripheral | Graph-based data integration could organize an evidence register; not RF or CI evidence. |
| 11 | 2017-01-13 9 p.m. | [Firetalk #4: 22 Short Films About Security](https://infocondb.org/con/shmoocon/shmoocon-xiii/firetalk-4-22-short-films-about-security) | Charlie Vedaa | Excluded | Broad retrospective on rejected security pitches; no specific CI/RF measurement method in the indexed abstract. |
| 12 | 2017-01-13 9:20 p.m. | [Firetalk #5: Slash AppSec Costs, Free Threat Modeling & Compliance Data Output](https://infocondb.org/con/shmoocon/shmoocon-xiii/firetalk-5-slash-appsec-costs-free-threat-modeling-compliance-data-output) | John Willis | Peripheral | System security requirements and threat modeling provide documentation context. |
| 13 | 2017-01-13 9:40 p.m. | [Firetalk #6: You Can Do the Thing!](https://infocondb.org/con/shmoocon/shmoocon-xiii/firetalk-6-you-can-do-the-thing) | Brendan O'Connor | Excluded | Civic participation exhortation; no technical link-analysis content. |
| 14 | 2017-01-14 10 a.m. | [LangSec for Penetration Testing: How and Why](https://infocondb.org/con/shmoocon/shmoocon-xiii/langsec-for-penetration-testing-how-and-why) | Falcon Darkstar Momot; Sergey Bratus | Methodological | Formal parser reasoning is transferable to protocol validation; no CI-specific protocol is established. |
| 15 | 2017-01-14 10 a.m. | [A Widening Attack Plain: Threatcasting Tomorrow's Threats](https://infocondb.org/con/shmoocon/shmoocon-xiii/a-widening-attack-plain-threatcasting-tomorrows-threats) | Brian David Johnson; Natalie Vanatta | Peripheral | Scenario-planning framework; future threat narratives are not observations. |
| 16 | 2017-01-14 10 a.m. | [So You Want to Hack Radios](https://infocondb.org/con/shmoocon/shmoocon-xiii/so-you-want-to-hack-radios) | Marc Newlin; Matt Knight | Direct | Explicit SDR/RF fundamentals and wireless analysis workflow; directly relevant to general RF characterization. |
| 17 | 2017-01-14 11 a.m. | [Ask the Feds](https://infocondb.org/con/shmoocon/shmoocon-xiii/ask-the-feds) | Allan Friedman; Nick Leiserson; Eric Mill; Jessica Wilkerson | Peripheral | Historical technology-policy panel; not current legal authority or RF evidence. |
| 18 | 2017-01-14 11 a.m. | [Exploring The Infrared World](https://infocondb.org/con/shmoocon/shmoocon-xiii/exploring-the-infrared-world) | Dominic Spill; Michael Ossmann | Methodological | Applies DSP to optical/infrared signals; useful methodological comparison, but not an RF or cochlear-link result. |
| 19 | 2017-01-14 11 a.m. | [Know Normal, Find Evil: Windows 10 Edition](https://infocondb.org/con/shmoocon/shmoocon-xiii/know-normal-find-evil-windows-10-edition) | Jake Williams | Peripheral | Baseline-first Windows investigation is an analogy for controls; domain differs from RF measurement. |
| 20 | 2017-01-14 noon | [Ask the EFF: Protecting Tomorrow](https://infocondb.org/con/shmoocon/shmoocon-xiii/ask-the-eff-protecting-tomorrow) | Andrew Crocker; Kurt Opsahl | Peripheral | Historical digital-rights panel; not current legal advice or a physical-link method. |
| 21 | 2017-01-14 noon | [Who Wants to Allow Arbitrary Code Execution on Their Boxes? We Do It Every Day.](https://infocondb.org/con/shmoocon/shmoocon-xiii/who-wants-to-allow-arbitrary-code-execution-on-their-boxes-we-do-it-every-day) | Brian Redbeard; Brad Ison | Excluded | Linux container isolation; no RF or cochlear-link connection in the abstract. |
| 22 | 2017-01-14 noon | [A Context-Aware Kernel IPC Firewall for Android](https://infocondb.org/con/shmoocon/shmoocon-xiii/a-context-aware-kernel-ipc-firewall-for-android) | David Wu; Sergey Bratus | Excluded | Android Binder IPC control; this software message path is not a wireless implant link. |
| 23 | 2017-01-14 2 p.m. | [Goodnight Moon & the House of Horrors: A look at the current IoT ecosystem and the regulations trying to control it](https://infocondb.org/con/shmoocon/shmoocon-xiii/goodnight-moon-the-house-of-horrors-a-look-at-the-current-iot-ecosystem-and-the-regulations-trying-to-control-it) | Aaron Alva; Whitney Merrill | Peripheral | Historical IoT security and policy context; device-specific transfer requires new evidence. |
| 24 | 2017-01-14 2 p.m. | [h·cek: Computing a Hacker Experience](https://infocondb.org/con/shmoocon/shmoocon-xiii/hcek-computing-a-hacker-experience) | Margaret Schedel; Melissa Clarke; Allison Miller | Excluded | Data-driven art and sonification; not evidence of physical auditory stimulation or RF coupling. |
| 25 | 2017-01-14 2 p.m. | [WaveConverter - An Open Source Software Tool for RF Reverse Engineering](https://infocondb.org/con/shmoocon/shmoocon-xiii/waveconverter-an-open-source-software-tool-for-rf-reverse-engineering) | Paul Clark | Direct | Processes recorded SDR I/Q using defined modulation and framing; directly relevant to offline RF characterization. |
| 26 | 2017-01-14 3 p.m. | [Plug-in Electric Vehicle Fingerprinting: Authentication for Plug-in Electric Vehicles](https://infocondb.org/con/shmoocon/shmoocon-xiii/plug-in-electric-vehicle-fingerprinting-authentication-for-plug-in-electric-vehicles) | Rebekah Houser | Methodological | Physical-device fingerprinting provides a comparison for classification validation; electric vehicles are a different system. |
| 27 | 2017-01-14 3 p.m. | [Flailing is Learning: My First Year as a Malware Analyst](https://infocondb.org/con/shmoocon/shmoocon-xiii/flailing-is-learning-my-first-year-as-a-malware-analyst) | Lauren Pearce | Excluded | Career/learning narrative in malware analysis; no RF-specific method. |
| 28 | 2017-01-14 3 p.m. | [I Have a Graph Database. Now What?](https://infocondb.org/con/shmoocon/shmoocon-xiii/i-have-a-graph-database-now-what) | Nicolas Kseib; Shimon Modi | Peripheral | Graph modeling may support evidence organization; links between records are not proof of physical causation. |
| 29 | 2017-01-14 4 p.m. | [Defeating Sandbox Evasion: How to Increase Successful Emulation Rate in Your Virtualized Environment](https://infocondb.org/con/shmoocon/shmoocon-xiii/defeating-sandbox-evasion-how-to-increase-successful-emulation-rate-in-your-virtualized-environment) | Alexander Chailytko; Stanislav Skuratovich | Excluded | Malware sandbox evasion; outside CI/NFMI RF characterization scope. |
| 30 | 2017-01-14 4 p.m. | [The State of Secure Messaging](https://infocondb.org/con/shmoocon/shmoocon-xiii/the-state-of-secure-messaging) | Nikita Borisov; Sze Chuen Tan | Peripheral | Cryptographic threat models provide background; internet messaging is distinct from implant telemetry. |
| 31 | 2017-01-14 4 p.m. | [0wn the Con](https://infocondb.org/con/shmoocon/shmoocon-xiii/0wn-the-con) | The Shmoo Group | Excluded | Conference operations and budgeting; no relevant interface evidence. |
| 32 | 2017-01-14 5 p.m. | [User Focused Security at Netflix: Stethoscope](https://infocondb.org/con/shmoocon/shmoocon-xiii/user-focused-security-at-netflix-stethoscope) | Andrew White; Jesse Kriss | Excluded | Endpoint-security usability tool; 'Stethoscope' is a product name, not medical instrumentation. |
| 33 | 2017-01-14 5 p.m. | [The Metadata is the Message (and Sometimes the Message is the Metadata)](https://infocondb.org/con/shmoocon/shmoocon-xiii/the-metadata-is-the-message-and-sometimes-the-message-is-the-metadata) | Matt Blaze | Peripheral | Historical content/metadata distinction supports provenance vocabulary; not current law or RF-source attribution. |
| 34 | 2017-01-14 5 p.m. | [Anti-Ransomware: Turning the Tables](https://infocondb.org/con/shmoocon/shmoocon-xiii/anti-ransomware-turning-the-tables) | Gal Shpantzer; G. Mark Hardy | Excluded | Enterprise ransomware mitigation; outside the bounded RF/CI workstream. |
| 35 | 2017-01-15 10 a.m. | [Dig Out Your Brick Phone! Bringing AMPS Back with GNU Radio](https://infocondb.org/con/shmoocon/shmoocon-xiii/dig-out-your-brick-phone-bringing-amps-back-with-gnu-radio) | Brandon Creighton / cstone | Methodological | GNU Radio protocol implementation is a historical comparison; AMPS is not NFMI or a CI link, and transmission is outside this task. |
| 36 | 2017-01-15 10 a.m. | [A Nickel Tour of the Ad Fraud Ecosystem](https://infocondb.org/con/shmoocon/shmoocon-xiii/a-nickel-tour-of-the-ad-fraud-ecosystem) | Ryan Castellucci | Excluded | Advertising fraud ecosystem; no RF measurement content. |
| 37 | 2017-01-15 10 a.m. | [ripr - Run Slices of Binary Code from Python](https://infocondb.org/con/shmoocon/shmoocon-xiii/ripr-run-slices-of-binary-code-from-python) | Patrick Biernat | Methodological | Offline binary-code extraction/emulation can support reproducible software analysis; no implant-specific demonstration. |
| 38 | 2017-01-15 11 a.m. | [Excuse me, Server, Do You Have the Time?](https://infocondb.org/con/shmoocon/shmoocon-xiii/excuse-me-server-do-you-have-the-time) | Brian Cardinale | Excluded | Predictable application tokens and server time; not RF timebase calibration or link synchronization evidence. |
| 39 | 2017-01-15 11 a.m. | [The Threat Intel Results are in… You are NOT the hacker! : Disinformation Campaigns vs. Attribution Claims](https://infocondb.org/con/shmoocon/shmoocon-xiii/the-threat-intel-results-are-in-you-are-not-the-hacker-disinformation-campaigns-vs-attribution-claims) | Mark Kuhr | Peripheral | Attribution uncertainty is relevant to reasoning discipline; this talk does not establish any actor in the present context. |
| 40 | 2017-01-15 11 a.m. | [Safety Bot Guaranteed](https://infocondb.org/con/shmoocon/shmoocon-xiii/safety-bot-guaranteed) | Rich Seymour | Peripheral | Safety-constraint documentation method; not validation of physical RF safety or clinical operation. |
| 41 | 2017-01-15 noon | [(In-)secure messaging with SCIMP and OMEMO](https://infocondb.org/con/shmoocon/shmoocon-xiii/in-secure-messaging-with-scimp-and-omemo) | Sebastian Verschoor | Methodological | Formal model-versus-implementation validation is transferable; the messaging protocols are unrelated to CI/NFMI. |
| 42 | 2017-01-15 noon | [Challenges and Opportunities: Application Containers and Micro Services](https://infocondb.org/con/shmoocon/shmoocon-xiii/challenges-and-opportunities-application-containers-and-micro-services) | Anil Karmel; Andrew Wild | Excluded | Container/microservice security; outside RF/CI measurement scope. |
| 43 | 2017-01-15 noon | [Does a BEAR Leak in the Woods? The Democratic National Committee breach, Russian APTs, and the 2016 U.S. Election](https://infocondb.org/con/shmoocon/shmoocon-xiii/does-a-bear-leak-in-the-woods-the-democratic-national-committee-breach-russian-apts-and-the-2016-us-election) | Toni Gidwani | Peripheral | Historical attribution case study; no basis for carrying actor claims into unrelated measurements. |
| 44 | 2017-01-15 1 p.m. | [Designing and Executing the World's First All-Computer Hacking Competition: A panel with the development team](https://infocondb.org/con/shmoocon/shmoocon-xiii/designing-and-executing-the-worlds-first-all-computer-hacking-competition-a-panel-with-the-development-team) | Tim Vidas / Vulc@n; Chris Eagle; Jason Wright; Brian Caswell; Mike Thompson; Holt Sorenson | Excluded | Automated software-hacking contest; no direct RF or cochlear-link characterization method. |

## Validation and delivery criteria

Assumption: relevance is judged against RF characterization of a known, documented CI/NFMI system, with adjacent methods retained only when their transfer is explicit.

Validation: 44 unique session URLs; continuous IDs 1–44; day counts 13/21/10; all 44 presenter fields populated; classification counts sum to 44; independent primary program corroborates focal presenter/date/time. The recording's mirror runtime is recorded separately from schedule duration. No clinical diagnosis, active RF work, external-device identification, or measurement validation was performed.

Delivery rubric: **coverage achieved** for this bounded index; **traceability achieved** through per-row URLs and web refs; **claim calibration achieved** by separating catalog, transcript, speaker assertion, and independent verification; **original-file reproducibility pending** because original media/slides/data and checksums were not obtained. Refinements improve the initial catalog-only reading by adding primary-program corroboration, actual mirror runtime, and explicit unfinished-work timestamps.


---

## Appendix B Medical-device conference audit

# Workstream B — medical-device security and bio-implant archive audit

Reviewed 20 November 2026. Targeted audit of 24 records. This report verifies identities, event metadata, artifact availability and narrowly scoped relevance; it does not claim a complete review of the entire InfoconDB graph or full video contents.

## Principal corrections

1. Barnaby Jack's Black Hat USA 2013 session was scheduled but not delivered. The official memorial states that the hour was left vacant. An archived abstract and the index's automated “Presented at” wording must not be treated as a recording or completed demonstration.
2. The 2025 Aguilar/Delifer workshop is **Medical Device Hacking: 201**. **Med Team vs Red Team** is the 2024 title.
3. Similarity links are not authorship. Correct neighboring presenters: Jason Gale (SAINTCON RFID, 2019), Robert Portvliet (ToorCon, 2017), Saurabh Harit (Black Hat Europe, 2017), Isabel Straw (MCH DBS workshop, 2022), and Jeremy Miller/Jonathan Fischer (Injectyll-HIDe, 2022).
4. Injectyll-HIDe concerns computer peripheral hardware, so it is excluded from biological-implant evidence. The MCH workshop describes DBS malfunction and exploratory security discussion; it does not establish malicious causation.
5. The final MCH organizer schedule is 22 July 2022, 22:30–23:30, whereas InfoconDB lists 23 July, 10:00. The latter must be retained as a conflicting secondary timestamp, not normalized silently.
6. DEF CON 28 belongs in the D0 N0 H4RM series. Joshua Corman is not listed in DC27/DC28; panel rosters vary. DC28 duration and roster conflict with the Outel mirror and remain unresolved without recording review.
7. The DerbyCon 2016 recorder page exposes a ham-radio title alongside the insulin-pump title. The exact delivered subject needs video verification.

## Applicability limits and validation

The study's Tier 1/2/3 model describes what a claim establishes, not whether a web page loads. These historical device and setting reports remain **Tier 2** for transfer to a new device or measurement. Governance recommendations are analyst synthesis; they are not a newly verified medical protocol. No item supplies Tier 1 evidence of an individual's implant or Tier 3-claim confirmation.

Primary sources confirm the strongest corrections (Black Hat cancellation; TROOPERS scope; Black Hat author identities; MCH final schedule). InfoconDB is used to verify **what the index says** when primary sources are unavailable. Such records are labeled, with access failures preserved. No exploit, active probing, device-control or transmission instructions are carried into the study.

Acceptance gates: every named lead has a disposition; each correction has a URL and source reference; rosters are edition-specific; available links are not called reviewed media; metadata conflicts remain visible. Quality rubric: provenance traceability—met; identity accuracy—met subject to marked conflicts; primary-source coverage—partial; full-video review—not performed; direct CI transfer—unsupported.

## Record register

### B01 — Medical Device Security: Hack or Hype?

- **Event / date:** TROOPERS16 · 2016-03-17 13:30
- **Presenters:** Kevin Fu
- **Review status:** primary abstract and slide text inspected. Confidence: high.
- **Study mapping:** Methods/governance: separate laboratory vulnerability, exploit, threat, and patient harm; preserve clinical workflow.
- **Disposition:** InfoconDB says duration unknown; organizer agenda allocates 13:30–14:30. Slides describe a laboratory demonstration without patients and caution against haphazard vulnerability scanning.
- **Index:** [record](https://infocondb.org/con/troopers/troopers16/medical-device-security-hack-or-hype)
- **Primary records / attempted access:** [source 1](https://troopers.de/events/troopers16/697_medical_device_security_hack_or_hype/) · [source 2](https://troopers.de/media/filer_public/f9/19/f919bcc6-a782-4d9c-a761-fa130de31a55/fu-med-sec-troopers-export-2016-small_.pdf)

### B02 — Implantable Medical Devices: Hacking Humans

- **Event / date:** Black Hat USA 2013 · 2013-08-01 planned 14:15
- **Presenters:** Barnaby Jack
- **Review status:** cancelled / scheduled abstract retained. Confidence: high.
- **Study mapping:** Archival quality control; no delivered results can be attributed to this session.
- **Disposition:** InfoconDB's automatic 'Presented at' label is misleading here. Official organizer notice left the hour vacant following Jack's death.
- **Index:** [record](https://infocondb.org/con/black-hat/black-hat-usa-2013/implantable-medical-devices-hacking-humans)
- **Primary records / attempted access:** [source 1](https://blackhat.com/us-13/archives.html) · [source 2](https://blackhat.com/latestintel/07262013-remembering-barnaby-jack.html)

### B03 — Hacking Medical Devices for Fun and Insulin: Breaking the Human SCADA System

- **Event / date:** Black Hat USA 2011 · 2011-08-03/04 event; exact session day not resolved
- **Presenters:** Jerome (Jay) Radcliffe
- **Review status:** primary program and white-paper identity inspected. Confidence: high.
- **Study mapping:** Methods: device-specific research and provenance; analysis is not evidence of CI protocol or RF carrier.
- **Disposition:** Use full title; primary record says Jerome Radcliffe. Do not describe the entire project as receive-only: the abstract discusses an intended injection attack and reports unfinished objectives.
- **Index:** No canonical index record resolved in this audit.
- **Primary records / attempted access:** [source 1](https://blackhat.com/html/bh-us-11/bh-us-11-archives.html) · [source 2](https://media.blackhat.com/bh-us-11/Radcliffe/BH_US_11_Radcliffe_Hacking_Medical_Devices_WP.pdf)

### B04 — Five year checkup: the state of insulin pump security

- **Event / date:** DerbyCon 6.0 Recharge · 2016-09-24 13:00
- **Presenters:** Jay Radcliffe
- **Review status:** index abstract inspected; recorder search result conflicts; playback unresolved. Confidence: medium.
- **Study mapping:** Governance: time- and generation-specific security changes require revalidation.
- **Disposition:** Recorder page title reports 'Hacking with Ham Radios: What I have learned in 25 years of being a ham' while retaining the insulin title below. Do not claim the indexed abstract was what was delivered without video review.
- **Index:** [record](https://infocondb.org/con/derbycon/derbycon-60-recharge/five-year-checkup-the-state-of-insulin-pump-security)
- **Primary records / attempted access:** [source 1](https://www.irongeek.com/i.php?page=videos%2Fderbycon6%2F210-five-year-checkup-the-state-of-insulin-pump-security-jay-radcliffe)

### B05 — Understanding and Exploiting Implanted Medical Devices

- **Event / date:** Black Hat USA 2018 · 2018-08-09 15:50
- **Presenters:** Billy Rios; Jonathan Butts
- **Review status:** primary abstract inspected; organizer video metadata located; no playback. Confidence: high.
- **Study mapping:** Governance: coordinated disclosure and device/infrastructure boundaries.
- **Disposition:** Add Jonathan Butts as coauthor. Findings concern named pacemaker/neurostimulator systems and supporting infrastructure, not all implants or cochlear implants.
- **Index:** [record](https://infocondb.org/con/black-hat/black-hat-usa-2018/understanding-and-exploiting-implanted-medical-devices)
- **Primary records / attempted access:** [source 1](https://blackhat.com/us-18/briefings.html) · [source 2](https://www.youtube.com/watch?v=l9XskAF-1Lc)

### B06 — An Examination of Infusion Pump Technology

- **Event / date:** Summercon 2015 · 2015-07-18 15:00–15:50
- **Presenters:** Billy Rios
- **Review status:** primary schedule confirmed; index abstract inspected. Confidence: high.
- **Study mapping:** Materials/governance comparator: hospital infusion architecture, not transcutaneous CI coupling.
- **Disposition:** Keep system class distinct; the current presentations archive does not expose the abstract in retrieved text, but official schedule confirms title and speaker.
- **Index:** [record](https://infocondb.org/con/summercon/summercon-2015/an-examination-of-infusion-pump-technology)
- **Primary records / attempted access:** [source 1](https://www.summercon.org/archives/2015/schedule.html) · [source 2](https://www.summercon.org/archives/2015/presentations.html)

### B07 — When IoT Attacks: Understanding the Safety Risks Associated with Connected Devices

- **Event / date:** Black Hat USA 2017 · 2017-07-26 11:15
- **Presenters:** Billy Rios; Jonathan Butts
- **Review status:** index abstract inspected; organizer artifact links located, not inspected. Confidence: high.
- **Study mapping:** Peripheral safety comparator; no CI RF inference.
- **Disposition:** Coauthor and subject category must be retained. General IoT physical-risk discussion is not a CI protocol reference.
- **Index:** [record](https://infocondb.org/con/black-hat/black-hat-usa-2017/when-iot-attacks-understanding-the-safety-risks-associated-with-connected-devices)
- **Primary records / attempted access:** Not opened.

### B08 — D0 No H4RM: A Healthcare Security Conversation

- **Event / date:** DEF CON 25 · 2017-07-29 20:00
- **Presenters:** Beau Woods; Michael C. McNeil; Jay Radcliffe; Suzanne Schwartz; Joshua Corman; Christian Dameff; Jeff Tully
- **Review status:** index metadata inspected; primary access incomplete. Confidence: high for index metadata.
- **Study mapping:** Execution/governance: multidisciplinary patient-safety discussion; not a measurement protocol.
- **Disposition:** 120 minutes; primary speaker page robots-denied.
- **Index:** [record](https://infocondb.org/con/def-con/def-con-25/d0-no-h4rm-a-healthcare-security-conversation)
- **Primary records / attempted access:** [source 1](https://defcon.org/html/defcon-25/dc-25-speakers.html)

### B09 — D0 N0 H4RM: A Healthcare Security Conversation

- **Event / date:** DEF CON 26 · 2018-08-10 20:00
- **Presenters:** Kirill Levchenko; Beau Woods; Roberto Suarez; Jay Radcliffe; David Nathans; Joshua Corman; Christian Dameff; Jeff Tully
- **Review status:** index metadata inspected; primary access incomplete. Confidence: high for index metadata.
- **Study mapping:** Execution/governance: multidisciplinary patient-safety discussion; not a measurement protocol.
- **Disposition:** Duration unknown in index; primary page unavailable.
- **Index:** [record](https://infocondb.org/con/def-con/def-con-26/d0-n0-h4rm-a-healthcare-security-conversation)
- **Primary records / attempted access:** [source 1](https://defcon.org/html/defcon-26/dc-26-speakers.html)

### B10 — D0 N0 H4RM: A Healthcare Security Conversation

- **Event / date:** DEF CON 27 · 2019-08-09 20:00
- **Presenters:** Marie Moe; Billy Rios; Jay Radcliffe; Suzanne Schwartz; Jeff Tully; Christian Dameff
- **Review status:** index metadata inspected; primary access incomplete. Confidence: high for index metadata.
- **Study mapping:** Execution/governance: multidisciplinary patient-safety discussion; not a measurement protocol.
- **Disposition:** 120 minutes in index; Joshua Corman not listed for this edition.
- **Index:** [record](https://infocondb.org/con/def-con/def-con-27/d0-n0-h4rm-a-healthcare-security-conversation)
- **Primary records / attempted access:** [source 1](https://defcon.org/html/defcon-27/dc-27-speakers.html)

### B11 — D0 N0 H4RM: A Healthcare Security Conversation

- **Event / date:** DEF CON 28 · 2020-08-07 20:00
- **Presenters:** Jeff Tully; Jessica Wilkerson; Veronica Schmitt; Ash Luft; Vidya Murthy; Christian Dameff
- **Review status:** index metadata inspected; primary access incomplete. Confidence: medium.
- **Study mapping:** Execution/governance: multidisciplinary patient-safety discussion; not a measurement protocol.
- **Disposition:** Index says 30 minutes with this roster. Outel mirror says 20:00–20:59 and a different panel; record version conflict. Video link available, not viewed.
- **Index:** [record](https://infocondb.org/con/def-con/def-con-28/d0-n0-h4rm-a-healthcare-security-conversation)
- **Primary records / attempted access:** [source 1](https://defcon.org/html/defcon-safemode/dc-safemode-speakers.html)

### B12 — D0 N0 H4RM: A Healthcare Security Conversation

- **Event / date:** DEF CON 29 · 2021-08-06 17:00
- **Presenters:** Jeff Tully; Jessica Wilkerson; Joshua Corman; Christian Dameff; Gabrielle Hempel; Stephanie Domas
- **Review status:** index metadata inspected; primary access incomplete. Confidence: high for index metadata.
- **Study mapping:** Execution/governance: multidisciplinary patient-safety discussion; not a measurement protocol.
- **Disposition:** 105 minutes in index; primary page robots-denied; Infocon recording links not reviewed.
- **Index:** [record](https://infocondb.org/con/def-con/def-con-29/d0-n0-h4rm-a-healthcare-security-conversation)
- **Primary records / attempted access:** [source 1](https://defcon.org/html/defcon-29/dc-29-speakers.html)

### B13 — D0 N0 H4RM: A Healthcare Security Conversation (Lounge)

- **Event / date:** DEF CON 30 · 2022-08-13 19:00
- **Presenters:** Jeff Tully; Alissa Knight; Seeyew Mo; Joshua Corman; Christian Dameff
- **Review status:** index metadata inspected; primary access incomplete. Confidence: high for index metadata.
- **Study mapping:** Execution/governance: multidisciplinary patient-safety discussion; not a measurement protocol.
- **Disposition:** 180-minute lounge in index; official forum returned 403.
- **Index:** [record](https://infocondb.org/con/def-con/def-con-30/d0-n0-h4rm-a-healthcare-security-conversation-lounge)
- **Primary records / attempted access:** [source 1](https://forum.defcon.org/node/242799)

### B14 — Anatomy of a Medical Device Hack- Doctors vs. Hackers in a Clinical Simulation Cage Match

- **Event / date:** DerbyCon 7.0 Legacy · 2017-09-23 18:00
- **Presenters:** Joshua Corman; Beau Woods; Jeff Tully; Christian Dameff
- **Review status:** index abstract inspected; organizer schedule timed out. Confidence: high.
- **Study mapping:** Execution: simulated incidents are training evidence, not observed patient attacks.
- **Disposition:** Preserve all four speakers and the explicit clinical-simulation design.
- **Index:** [record](https://infocondb.org/con/derbycon/derbycon-70-legacy/anatomy-of-a-medical-device-hack-doctors-vs-hackers-in-a-clinical-simulation-cage-match)
- **Primary records / attempted access:** [source 1](https://www.derbycon.com/saturday-schedule/)

### B15 — I Am The Cavalry Track Welcome and Overview

- **Event / date:** BSidesLV 2019 · 2019-08-06 11:30
- **Presenters:** Beau Woods; Joshua Corman
- **Review status:** index abstract inspected; video access throttled. Confidence: high.
- **Study mapping:** Governance track orientation; no primary signal-processing result.
- **Disposition:** This is one 25-minute introductory session, not evidence that every track talk was reviewed.
- **Index:** [record](https://infocondb.org/con/security-bsides/bsideslv-2019/i-am-the-cavalry-track-welcome-and-overview)
- **Primary records / attempted access:** [source 1](https://www.youtube.com/watch?v=m08pLyV-Rrg)

### B16 — Med Team vs Red Team: Intro into Medical Device Hacking

- **Event / date:** DEF CON 32 · 2024-08-08 09:00
- **Presenters:** Alex Delifer; Michael "v3ga" Aguilar
- **Review status:** index workshop abstract inspected; primary page restricted. Confidence: high.
- **Study mapping:** Only borrow isolated authorized Device Lab governance, not active testing procedures.
- **Disposition:** Four-hour workshop; does not authorize testing any person's medical device.
- **Index:** [record](https://infocondb.org/con/def-con/def-con-32/med-team-vs-red-team-intro-into-medical-device-hacking)
- **Primary records / attempted access:** [source 1](https://defcon.org/html/defcon-32/dc-32-workshops.html)

### B17 — Medical Device Hacking: 201

- **Event / date:** DEF CON 33 · 2025-08-08 09:00
- **Presenters:** Michael "v3ga" Aguilar; Alex "cheet" Delifer
- **Review status:** index workshop abstract inspected; primary pages unavailable. Confidence: high.
- **Study mapping:** Governance comparator only.
- **Disposition:** Correct 2025 title; not the same title as DC32. Preserve Alex's alias without creating a separate human identity.
- **Index:** [record](https://infocondb.org/con/def-con/def-con-33/medical-device-hacking-201)
- **Primary records / attempted access:** [source 1](https://defcon.org/html/defcon-33/dc-33-workshops.html) · [source 2](https://events.humanitix.com/dc33ws-n260-08a)

### B18 — Designing RFID Implants - How flipping the bird opens doors for me

- **Event / date:** DEF CON 31 · 2023-08-10 14:30
- **Presenters:** Miana Ella Windall
- **Review status:** index abstract and primary search text verified; direct forum fetch 403. Confidence: high.
- **Study mapping:** Materials comparator: RFID credentials are distinct from CI stimulation systems.
- **Disposition:** 45-minute War Stories talk. Similar-presentations graph is a topical edge, not authorship evidence.
- **Index:** [record](https://infocondb.org/con/def-con/def-con-31/designing-rfid-implants-how-flipping-the-bird-opens-doors-for-me)
- **Primary records / attempted access:** [source 1](https://forum.defcon.org/node/246100)

### B19 — NFC & RFID Bio-Implants: For Fun and Profit

- **Event / date:** SAINTCON 2019 · 2019-10-24 10:00
- **Presenters:** Jason Gale
- **Review status:** index metadata inspected; official schedule 403; video not inspected. Confidence: high.
- **Study mapping:** RFID comparator only; no inferred CI carrier or coupling performance.
- **Disposition:** Jason Gale is the indexed presenter, not Miana Windall.
- **Index:** [record](https://infocondb.org/con/saintcon/saintcon-2019/nfc-rfid-bio-implants-for-fun-and-profit)
- **Primary records / attempted access:** [source 1](https://saintcon2019.sched.com/event/W6Ua/nfc-rfid-bio-implants-for-fun-and-profit) · [source 2](https://www.youtube.com/watch?v=CaYK-tNvG5o)

### B20 — Injectyll-HIDe: Pushing the Future of Hardware Implants to the Next Level

- **Event / date:** DEF CON 30 · 2022-08-13 10:00
- **Presenters:** Jeremy Miller; Jonathan Fischer
- **Review status:** index abstract inspected; official forum search corroborates title/authors; direct access 403. Confidence: high.
- **Study mapping:** EXCLUDE from biological-implant evidence: computer peripheral/red-team hardware.
- **Disposition:** The word implant describes computer intrusion hardware here. No connection to Miana Windall or neural implants.
- **Index:** [record](https://infocondb.org/con/def-con/def-con-30/injectyll-hide-pushing-the-future-of-hardware-implants-to-the-next-level)
- **Primary records / attempted access:** [source 1](https://forum.defcon.org/node/239774)

### B21 — Can’t get you out of my head: Telemetric hacking of medical deep brain stimulators

- **Event / date:** MCH2022 · 2022-07-22 22:30–23:30 official; index differs
- **Presenters:** Isabel Straw
- **Review status:** primary workshop schedule and abstract inspected. Confidence: high.
- **Study mapping:** Governance: clinical malfunction and speculative security threat are separate categories.
- **Disposition:** Official final schedule differs from index July 23 10:00. Abstract describes malfunction and brainstorming, explicitly discussing theoretical attacks; not a demonstrated malicious-patient-attack report. Author is Isabel Straw.
- **Index:** [record](https://infocondb.org/con/dutch-hacker-camps/may-contain-hackers-mch2022/cant-get-you-out-of-my-head-telemetric-hacking-of-medical-deep-brain-stimulators)
- **Primary records / attempted access:** [source 1](https://program.mch2022.org/mch2022/talk/XCR8P7/)

### B22 — Open Up and Say 0×41414141: Attacking Medical Devices

- **Event / date:** ToorCon San Diego 19 · 2017-09-02 13:00
- **Presenters:** Robert Portvliet
- **Review status:** index abstract inspected; original conference URL 404. Confidence: high.
- **Study mapping:** Governance comparator: classify network, device, and supporting-system scope separately.
- **Disposition:** Presenter is Robert Portvliet, not Delifer/Aguilar. Active penetration testing material does not become receive-only methodology by similarity.
- **Index:** [record](https://infocondb.org/con/toorcon/toorcon-san-diego-19/open-up-and-say-041414141-attacking-medical-devices)
- **Primary records / attempted access:** [source 1](https://sandiego.toorcon.net/conference/)

### B23 — Breaking Bad: Stealing Patient Data Through Medical Devices

- **Event / date:** Black Hat Europe 2017 · 2017-12-06 10:15
- **Presenters:** Saurabh Harit
- **Review status:** primary briefing abstract inspected. Confidence: high.
- **Study mapping:** Data/governance: clinical data confidentiality is a distinct risk from therapeutic control.
- **Disposition:** Author is Saurabh Harit, not Delifer/Aguilar; primary emphasis is patient-record access.
- **Index:** [record](https://infocondb.org/con/black-hat/black-hat-europe-2017/breaking-bad-stealing-patient-data-through-medical-devices)
- **Primary records / attempted access:** [source 1](https://blackhat.com/archive/europe/2017/briefings.html)

### B24 — Unpatchable Living with a vulnerable implanted device

- **Event / date:** TROOPERS16 · 2016-03-17 16:00
- **Presenters:** Marie Moe
- **Review status:** primary abstract and slide link inspected; slides not read. Confidence: high.
- **Study mapping:** Added patient-experience/incident-sharing comparator; no direct CI measurements.
- **Disposition:** Published account of a known implant; do not generalize presence or vulnerability to another individual.
- **Index:** No canonical index record resolved in this audit.
- **Primary records / attempted access:** [source 1](https://troopers.de/events/troopers16/696_unpatchable_living_with_a_vulnerable_implanted_device/)

## Open verification items

- Full video review and timestamped extraction for the delivered sessions are outstanding. In particular, resolve DerbyCon 2016's competing title and DC28's roster/duration.
- Official DEF CON speaker pages were robots-denied or restricted; several forum endpoints returned 403. These failures do not establish absence of the session or artifact.
- SAINTCON's official schedule returned 403, ToorCon's old conference path returned 404, and DerbyCon's schedule timed out. Indexed metadata is retained with reduced verification depth.
- Talk-specific CI carrier frequencies, near-field geometry, receiver performance, encryption and present-day vulnerability cannot be inferred from these analogies.

## Practical mapping to the five study pillars

| Pillar | Defensible use | Validation needed before transfer |
|---|---|---|
| Materials | Separate CI, pacemaker, infusion-pump, RFID credential and computer-peripheral systems. | Exact device model and public technical documentation. |
| Methods | Preserve isolation, consented scope and distinction between observational work and active tests. | Receive chain controls and independent signal provenance. |
| Data | Record metadata source, author, program revision and artifact type. | Hash captured files and metadata separately; hashes do not prove historical truth. |
| Analysis | Treat security claims as generation-specific; keep malfunction separate from adversarial cause. | Independent measurements and alternative-explanation controls. |
| Execution | Use multidisciplinary clinical/safety review where a verified medical device is involved. | Approved scope and qualified oversight; no patient-device interaction is authorized by this archive. |



---

## Appendix C Radio-analysis conference audit

# Workstream C — RF conference and tool provenance audit

Review date: 20 November 2026. Scope: the named RF/SDR conference renditions in the task specification. Twenty-four individual conference records, five presenter profiles, and three tool projects were examined. This is a targeted archival audit, not a census of every RF talk in InfoconDB.

The strongest reusable result is an evidence sequence: document the receiver and source assumptions, characterize the recorded channel, assess modulation and timing, and retain enough raw data for an independent analyst to reproduce the interpretation. The conference material supplies methodological precedents; it does not validate the supplied study's numerical results or identify a medical device.

## Findings requiring changes in the master compilation

1. Restore the coauthors omitted by presenter-centric summaries: Dominic Spill for the 2017 Black Hat signal-identification talk and 2018 *Revolting Radios*; Sergey Bratus for the 2015 REcon polyglot talk; Christiane Ruetten for the 2016 TROOPERS DMR talk.
2. Attribute *Lazy-Mode RF OSINT and Reverse Engineering* to Marc Newlin alone. The LoRa talks are Matt Knight's. A “Similar Presentations” link is neither an authorship relation nor corroborating evidence.
3. Preserve unknown dates and durations. InfoconDB lacks exact scheduling for the checked 44CON 2017 rendition and Black Hat Asia 2015 rendition. The 33C3 programme gives a 60-minute slot, whereas its media page lists 64 minutes.
4. Record tool provenance accurately. URH's official repository is archived/read-only, dated 29 March 2026. Its release listing shows v2.10.0; that supports a reproducible historical pin, not an assumption of active maintenance. Evaluate third-party forks independently.
5. Do not attach the supplied study's Hann-window calculations, custom hashing scripts, exact synthetic thresholds, or clinical decision rules to conference abstracts that do not contain them. Cite the study code, mathematical derivation, applicable standards, or clinical authority separately.

## Source-grounded method mapping

| Study layer | Source-supported insight | Application in this study | Limit |
|---|---|---|---|
| Materials | Ossmann's TROOPERS16 abstract describes combining SDR and non-SDR tools. | Identify which observable each instrument measures and document its validated operating range. | It does not make an oscilloscope mandatory at a universal sampling rate or bandwidth. |
| Methods | Knight/Newlin TROOPERS17 slides place public-source research before channel/modulation/timing analysis. | Retain the precise manufacturer/FCC source and treat its values as hypotheses to check. | A regulatory match does not establish emitter identity. |
| Data | SigMF specifies typed samples and structured recording metadata. | Record datatype, sample rate, relevant capture indices, schema version and dataset digest. | Metadata can be internally consistent and still factually wrong; a hash proves byte stability, not origin. |
| Analysis | Spill/Ossmann BH2017 slides distinguish signal descriptors from protocol identification and show waterfall limitations. | Report observed frequency/bandwidth/timing before candidate protocol labels; retain original samples. | Automated classification does not establish causation, implant presence, or neural decoding. |
| Timing | Knight/Newlin TROOPERS17 slides distinguish data-bit rate from encoded symbol timing. | Report timing uncertainty and line-code hypothesis explicitly. | Their Z-Wave example is not a CI protocol specification. |
| Execution | inspectrum supports saved-recording plots and timing cursors; URH offers separable interpretation and analysis functions. | Use offline analysis with original files preserved. | Generation, fuzzing, transmission, replay, firmware modification and patient-connected probing are outside scope. |

Sources for this mapping: [TROOPERS16](https://troopers.de/events/troopers16/532_rapid_radio_reversing/), [TROOPERS17 primary slides](https://troopers.de/downloads/troopers17/TR17_SoYou_Want_To_Hack_Radios.pdf), [Black Hat 2017 primary slides](https://www.blackhat.com/docs/us-17/wednesday/us-17-Ossmann-Whats-On-The-Wireless-Automating-RF-Signal-Identification.pdf), [SigMF specification](https://sigmf.org/index.html), [inspectrum](https://github.com/miek/inspectrum), [URH paper](https://www.usenix.org/conference/woot18/presentation/pohl).

## Verified conference register

Dates/times below are the index's scheduled local values; their timezones were not independently verified. “Unknown” is retained. The JSON companion carries per-record availability, source references and limits. A media link was not treated as proof that its full content was inspected.

| ID | Event / scheduled date | Presentation | Credited presenters | Source access |
|---|---|---|---|---|
| C01 | REcon 2014 / 2014-06-27 11:30 | [SDR Tricks with HackRF](https://infocondb.org/con/recon/recon-2014/sdr-tricks-with-hackrf) | Michael Ossmann | primary programme and slides/recording links |
| C02 | BSidesLV 2015 / 2015-08-05 11:30 | [Better Spectrum Monitoring with Software Defined Radio](https://infocondb.org/con/security-bsides/bsideslv-2015/better-spectrum-monitoring-with-software-defined-radio) | Michael Ossmann | index abstract and video links; primary schedule fetch 403 |
| C03 | ToorCon San Diego 17 / 2015-10-24 15:00 | [Rapid Radio Reversing](https://infocondb.org/con/toorcon/toorcon-san-diego-17/rapid-radio-reversing) | Michael Ossmann | index abstract; author's presentations page corroborates event and links video |
| C04 | TROOPERS16 / 2016-03-17 13:30 | [Rapid Radio Reversing](https://infocondb.org/con/troopers/troopers16/rapid-radio-reversing) | Michael Ossmann | primary event abstract |
| C05 | Black Hat USA 2017 / 2017-07-26 14:40 | [What's on the Wireless? Automating RF Signal Identification](https://infocondb.org/con/black-hat/black-hat-usa-2017/whats-on-the-wireless-automating-rf-signal-identification) | Dominic Spill; Michael Ossmann | primary 32-page slide deck text inspected |
| C06 | REcon 2017 / 2017-06-18 16:30 | [Reverse Engineering DSSS](https://infocondb.org/con/recon/recon-2017/reverse-engineering-dsss) | Michael Ossmann | primary abstract; index lists slides and video |
| C07 | DEF CON 26 / 2018-08-10 14:00 | [Revolting Radios](https://infocondb.org/con/def-con/def-con-26/revolting-radios) | Michael Ossmann; Dominic Spill | index abstract and video links; primary page fetch restricted |
| C08 | ShmooCon XIII / 2017-01-14 10:00 | [So You Want to Hack Radios](https://infocondb.org/con/shmoocon/shmoocon-xiii/so-you-want-to-hack-radios) | Marc Newlin; Matt Knight | index abstract/video; author-organization repository search corroborates; repository direct fetch unavailable |
| C09 | TROOPERS17 / 2017-03-20 11:30 | [So You Want to Hack Radios](https://infocondb.org/con/troopers/troopers17/so-you-want-to-hack-radios) | Matt Knight; Marc Newlin | primary event page and 126-page slides text inspected |
| C10 | 44CON 2017 / Unknown  | [So You Want to Hack Radios](https://infocondb.org/con/44con/44con-2017/so-you-want-to-hack-radios) | Marc Newlin; Matt Knight | primary event abstract; index lists video/subtitles |
| C11 | DEF CON 25 / 2017-07-28 16:00 | [Radio Exploitation 101: Characterizing, Contextualizing, and Applying Wireless Attack Methods](https://infocondb.org/con/def-con/def-con-25/radio-exploitation-101-characterizing-contextualizing-and-applying-wireless-attack-methods) | Matt Knight; Marc Newlin | index abstract and video links; primary page restricted |
| C12 | TROOPERS18 / 2018-03-13 16:00 | [Lazy-Mode RF OSINT and Reverse Engineering](https://infocondb.org/con/troopers/troopers18/lazy-mode-rf-osint-and-reverse-engineering) | Marc Newlin | primary event abstract; slide retrieval 502; video label 'coming soon' |
| C13 | 33C3 / 2016-12-29 18:30 | [Decoding the LoRa PHY: Dissecting a Modern Wireless Network for the Internet of Things](https://infocondb.org/con/ccc/33c3/decoding-the-lora-phy-dissecting-a-modern-wireless-network-for-the-internet-of-things) | Matt Knight | primary event and media pages; recording listed 64 min versus 60-min scheduled slot |
| C14 | ToorCon San Diego 18 / 2016-10-15 11:00 | [Decoding LoRa, A Modern Wireless Network for the Internet of Things](https://infocondb.org/con/toorcon/toorcon-san-diego-18/decoding-lora-a-modern-wireless-network-for-the-internet-of-things) | Matt Knight | index abstract only |
| C15 | DEF CON 21 / 2013-08-02 10:00 | [All Your RFz Are Belong to Me - Hacking the Wireless World with Software Defined Radio](https://infocondb.org/con/def-con/def-con-21/all-your-rfz-are-belong-to-me-hacking-the-wireless-world-with-software-defined-radio) | Balint Seeber | index abstract and media links; primary not opened |
| C16 | Black Hat USA 2014 / 2014-08-07 17:00 | [Hacking the Wireless World with Software Defined Radio - 2.0](https://infocondb.org/con/black-hat/black-hat-usa-2014/hacking-the-wireless-world-with-software-defined-radio-20) | Balint Seeber | index abstract; primary slide retrieval failed |
| C17 | Black Hat Europe 2014 / 2014-10-16 14:15 | [Hacking the Wireless World with Software Defined Radio - 2.0](https://infocondb.org/con/black-hat/black-hat-europe-2014/hacking-the-wireless-world-with-software-defined-radio-20) | Balint Seeber | primary conference abstract |
| C18 | Black Hat Asia 2015 / Unknown  | [Hacking the Wireless World with Software Defined Radio - 2.0](https://infocondb.org/con/black-hat/black-hat-asia-2015/hacking-the-wireless-world-with-software-defined-radio-20) | Balint Seeber | primary abstract; index has no date/time/duration or abstract |
| C19 | BSidesLV 2015 / 2015-08-05 16:00 | [All Your RFz Are Belong to Me – Software Defined Radio Exploits](https://infocondb.org/con/security-bsides/bsideslv-2015/all-your-rfz-are-belong-to-me-software-defined-radio-exploits) | Balint Seeber | index abstract, schedule and media links; primary not opened |
| C20 | ShmooCon XII / 2016-01-16 11:00 | [Hacking The Wireless World - Software Defined Radio Exploits](https://infocondb.org/con/shmoocon/shmoocon-xii/hacking-the-wireless-world-software-defined-radio-exploits) | Balint Seeber | index abstract and video/subtitle links |
| C21 | Black Hat USA 2018 / 2018-08-09 15:50 | [SirenJack: Cracking a 'Secure' Emergency Warning Siren System](https://infocondb.org/con/black-hat/black-hat-usa-2018/sirenjack-cracking-a-secure-emergency-warning-siren-system) | Balint Seeber | primary abstract; dynamic schedule lost session data; index media links |
| C22 | REcon 2015 / 2015-06-19 16:00 | [Polyglots and Chimeras in Digital Radio Modes: Featuring Practical Matryoshka Protocols for a 21st Century Numbers Station](https://infocondb.org/con/recon/recon-2015/polyglots-and-chimeras-in-digital-radio-modes-featuring-practical-matryoshka-protocols-for-a-21st-century-numbers-station) | Travis Goodspeed; Sergey Bratus | primary event abstract |
| C23 | TROOPERS16 / 2016-03-16 17:00 | [Reverse Engineering a Digital Two-Way Radio](https://infocondb.org/con/troopers/troopers16/reverse-engineering-a-digital-two-way-radio) | Travis Goodspeed; Christiane Ruetten | primary event abstract |
| C24 | Summercon 2016 / 2016-07-15 16:00 | [Mad Dog 380; or, Patching a Handheld Digital Radio](https://infocondb.org/con/summercon/summercon-2016/mad-dog-380-or-patching-a-handheld-digital-radio) | Travis Goodspeed | primary presentation abstract |

## Tool records

- **C-T01 URH:** [Official repository](https://github.com/jopohl/urh), [release history](https://github.com/jopohl/urh/releases), and [WOOT18 paper](https://www.usenix.org/conference/woot18/presentation/pohl). Johannes Pohl and Andreas Noack are credited by USENIX. v2.10.0 is listed as latest; repository archive status is explicit. No executable was installed or run in this workstream.
- **C-T02 inspectrum:** [Official repository](https://github.com/miek/inspectrum), maintained under [Mike Walters's account](https://github.com/miek). Documentation lists saved-signal spectrograms, amplitude/frequency/phase/IQ views, timing cursors and SigMF/raw sample inputs. File extensions and assumed sample rates still require explicit provenance.
- **C-T03 SigMF:** [Official releases](https://github.com/sigmf/SigMF/releases) list v1.2.6; [specification](https://sigmf.org/index.html) describes the dataset SHA-512 field. A collection's recording-object `hash` instead references metadata. Ben Hilburn's conference-history role was not independently established here; use project/contributor attribution unless a primary historical source is added.

## Assumptions, validation and disposition

**Assumptions.** The study is archival and receive-only. A historical device demonstration applies to the documented configuration, not an unidentified system. Repeated conference renditions are not independent experimental replications.

**Validation criteria.** A title/event/author record passes archival identification when the index is resolved and its attribution is explicit. A methodological claim requires an opened primary abstract, slide deck, paper or project documentation. Video contents, performance claims, tuning limits and sample calculations require separate evidence.

**Validation performed.** All 24 named conference records resolved in InfoconDB; primary corroboration and failures are documented record by record. Two primary RF slide decks were text-inspected. No full video playback, RF capture, hardware testing, or protocol decoding was performed. Scheduled metadata is not evidence that every claimed demonstration succeeded.

**Access gaps.** DEF CON speaker pages for 2017/2018 were restricted through this retrieval path. BSidesLV 2015's schedule returned 403. The TROOPERS18 slide URL returned 502. The Black Hat USA 2018 dynamic schedule returned no sessions, but its static briefings archive retained the SirenJack abstract. The Black Hat USA 2014 PDF failed retrieval. ToorCon2016 LoRa and several Seeber renditions remain index-level in this pass. Original recording files were not hashed.

**Delivery rubric.** Attribution: corrected and traceable. Source hierarchy: primary sources distinguished from discovery records. Completeness: all assigned renditions covered, full-history/video review not claimed. Reproducibility: machine-readable records preserve URLs, nulls and source refs. Scope control: only general passive methods transferred; device and clinical conclusions excluded. These refinements improve the prior compilation by preventing coauthor loss, repeated-talk double counting, unsupported method attribution and false completion claims.



---

## Appendix D Technical claim register

# Independent technical claim audit

As of **20 November 2026**. Scope: primary vendor/specification checks plus independent arithmetic. No hardware interaction or live RF capture was performed.

## Assumptions and acceptance criteria

- The supplied task is a draft to audit, not independently established evidence.
- Versions are checked as of 2026-11-20; official release existence is separate from local execution.
- Physical-law examples use simplified free-space geometry; patient-specific effects are not inferred.

A claim passes when an opened primary source supports its specific scope, or a disclosed independent calculation reproduces it. Software-version existence is not a test result. Device-specific claims remain unmeasured. Corrections improve the draft by separating model, configuration, method and evidentiary limits.

## Correction register

| ID | Dimension | Disposition | Draft claim | Corrected finding | Sources | Validation/action |
|---|---|---|---|---|---|---|
| TA01 | Materials | CORRECT | SMArt v5 floor is approximately 25 MHz; R820T2/R828D. | SMArt v5 overall coverage is 100 kHz–1.75 GHz, with direct sampling below 25 MHz. Tuner-mode coverage and direct-sampling coverage must be separate. Manufacturer lists R820T2/R860 in product detail, R820T2 in its table; R828D belongs to Blog V4. | T01;T02 | Record exact unit, tuner reported by driver, mode and driver. Do not treat an HF direct-sampling check as proof of tuner-mode HF reception. |
| TA02 | Materials | QUALIFY | XTR universally starts at 65 MHz; gap 1100–1250 MHz. | Official Nooelec sources disagree: 55 MHz in support/spec table versus approximately 65 MHz in product narrative; support gap is 1100–1200 MHz. Both published lower limits exclude 49 MHz and 13.56 MHz. | T02;T03 | Carry the manufacturer discrepancy explicitly; characterize the actual unit on a bench reference before adopting a numerical tuning boundary. |
| TA03 | Materials | CONFIRM WITH AXIS CONTROL | Ham It Up adds 125 MHz. | The mixing LO is +125 MHz; the RF display correction is -125 MHz. Store tuner frequency, LO offset, conversion mode and inferred RF frequency separately. | T04 | Verify absolute-axis calculation against a known reference; avoid applying the offset twice. |
| TA04 | Materials | CORRECT | RTL-SDR V4/V4L introduced August 2026. | V4: August 2023, R828D. V4L: 11 August 2026, R828S. Both use built-in HF upconversion; V4L has different front-end filtering. | T05;T06 | Record precise model rather than the combined V4/V4L label. |
| TA05 | Materials | CONFIRM | V1.4.0 Windows driver is relevant to V4L. | The official V1.4.0 release explicitly adds V4L support. Platform architecture and SDR application library must match. Driver availability is not evidence that the connected unit has been enumerated successfully. | T07;T08 | Archive installed DLL/library version or hash and actual enumeration output. |
| TA06 | Materials | QUALIFY | RSP1B is 14-bit at all supported sample rates. | Datasheet specifies 2–10.66 MS/s: 14-bit at 2–6.048, 12-bit at 6.048–8.064, 10-bit at 8.064–9.216, 8-bit above 9.216 MS/s. API output storage width does not equal ADC resolution. | T09 | Report ADC mode, device rate, decimation and stored sample dtype separately. |
| TA07 | Materials | PARTLY VERIFIED | RSP1B and RSPdx can share every ADC setting claim. | RSPdx manufacturer launch confirms 1 kHz–2 GHz coverage and 14-bit architecture, but the old detailed datasheet URL returned 404 in this audit. Do not silently inherit every RSP1B setting from a product-family label. | T09;T10;T24 | Retain RSP1B rate-resolution table as verified; retrieve the exact RSPdx hardware manual before repeating its detailed table. |
| TA08 | Materials | CORRECT | DS1054Z exemplifies a required ≥100 MHz oscilloscope. | The DS1054Z model is specified at 50 MHz. The draft combines a historical 50 MHz instrument with an unsupported universal ≥100 MHz requirement. | T11 | State the historical model accurately; derive any new instrument requirement from the specific measurand and permitted error. |
| TA09 | Methods | REPLACE | ≥20 MS/s and ≥100 MHz analog bandwidth are universally sufficient. | Digital rate, analog bandwidth, rise time, signal bandwidth and alias rejection are separate constraints. Ordinary real sampling of a 49 MHz carrier needs more than 98 MS/s before practical margin; intentional bandpass sampling requires a separately justified design. For envelope edges, use the edge spectrum/rise time, not carrier frequency alone. | T12;independent sampling analysis | Specify direct RF versus envelope input and the fastest feature to resolve. No fixed rate makes all measurements adequate. |
| TA10 | Methods | CORRECT/QUALIFY | At 2.4 MS/s a ~1.1 Mbps Manchester signal has ample edge detail. | At 1.1 Mbps, one Manchester half-bit is about 454.5 ns and has only 1.09 samples at 2.4 MS/s; 0.5 Mbps gives 2.4 samples per half-bit. Those counts do not validate rise-time or ringing reconstruction. | independent arithmetic | Require a validated recovery model, analog filter response, clock/jitter characterization and uncertainty before claiming detailed edge measurements. |
| TA11 | Software | CORRECT | SDR++ 1.3.2 is a fixed reproducible version pin. | The official page identifies 1.3.2 as a mutable nightly. Version text alone does not fix the binary; its linked source archive also carries a synchronization warning. | T13 | Pin source commit, platform asset filename, build timestamp, SHA-256 and dependent libraries. Preserve a tested artifact. |
| TA12 | Software | CONFIRM | Gqrx 2.17.7 exists and fixes Apple Silicon launch. | Official release includes an ARM Mac DMG startup fix and remote-control start/stop of I/Q recording. Release existence does not establish local installation or a successful capture. | T14 | Record actual installed app version and capture provenance. |
| TA13 | Software | CONFIRM WITH DATE | Python 3.12.14 is a valid as-of-2026 pin. | Official release is dated 12 August 2026 and is superseded by 3.12.16. It is a valid historical environment pin, not the latest release. | T15 | Record interpreter executable/version actually used. Re-running with a newer interpreter is a distinct compatibility check. |
| TA14 | Software | CONFIRM WITH TEST STATUS | NumPy 2.3.5 and 2.5.5 are valid versions. | Both have official release notes. NumPy 2.5.5 was released 15 November 2026. Existence and documented Python support do not prove the study ran under both versions. | T16;T17 | Mark compatibility as tested only when per-environment logs and output comparisons exist. |
| TA15 | Software | PARTLY CONFIRM | Pillow 13.0.0 is a valid pin; deterministic pixels guaranteed. | 13.0.0 was released 16 October 2026. Pixel determinism remains an implementation/environment claim requiring output hashes; pinning Pillow alone cannot prove identical fonts, encoders or output metadata. | T18 | Compare numerical outputs separately from rendered-file byte identity; record fonts and image encoding settings if exact images matter. |
| TA16 | Physics | CORRECT DOMAIN | NFMI always falls as 1/r³ throughout the near field. | The magnetic dipole approximation requires distance large relative to source dimensions while remaining in the reactive near field. For a circular loop on axis, B(z)=μ0 N I a²/[2(a²+z²)^(3/2)]; only z≫a gives z^-3. Millimeter coil gaps may not meet that condition. | T20;T23;independent derivation | State geometry, medium and applicable distance regime; no inverse-cube extrapolation from one arbitrary capture. |
| TA17 | Methods | CORRECT | A passive/receive-only pickup guarantees no electromagnetic interaction. | Receive-only excludes intentional transmission; a coupled receiving loop can still load or detune a resonant circuit. Manufacturer NFC examples document geometry-dependent loading; they do not quantify effects on an implanted clinical device. | T20;T22 | Keep this execution offline/archival. Any physical device-specific protocol requires separate qualified engineering and clinical assessment; do not label it zero-interaction by assumption. |
| TA18 | Materials | QUALIFY | A multi-turn shielded loop or ferrite rod is universally the correct probe. | Probe choice depends on frequency response, aperture, orientation, loading and desired electric/magnetic selectivity. More turns or ferrite is not automatically better across 148.5 kHz–60 MHz. | T20;T21;T22 | For an authorized bench fixture, document probe transfer function, orientation, distance and uncertainty; avoid a universal build prescription. |
| TA19 | Data | CONFIRM | core:sha512 is the correct SigMF field. | SigMF v1.2.6 defines global core:sha512 for the dataset digest. core:hash is not a listed core global field. A collection recording object's hash is a separate field for metadata, not an interchangeable global field. | T19 | Validate required fields/namespaces and recompute the digest. Do not call this a historical migration from v1.0.0 without checking that older specification. |
| TA20 | Data | CORRECT | QI order can be a compliant core SigMF complex dataset. | Core SigMF complex storage requires I then Q. A custom analyzer may accept QI, but those bytes cannot simply be relabeled compliant cf32_le. The 32 denotes each component, so a cf32_le complex sample occupies eight bytes. | T19 | Reorder to canonical I/Q for a compliant output, preserving the original file and explicit conversion provenance. |
| TA21 | Data | CORRECT | Replacing hash and checking sample_count ensures full compliance. | Schema and recording compliance also depend on required fields, namespaces, file naming and on-disk representation. A custom sanity check or a valid JSON file is not a complete conformance test. | T19 | Use the versioned schema and semantic checks; check data size, channel count, offsets/headers/trailers, hashes and annotation extent. Report which checks actually ran. |
| TA22 | Data | QUALIFY | Unknown values should always be null or UNKNOWN. | Custom provenance fields may use documented sentinels; typed standard numeric/time fields must obey their schema. Omit an optional unknown field rather than insert a string or null that violates its type. | T19;independent schema reasoning | Schema-validate the final record; keep unresolved provenance explicit outside incompatible typed fields. |
| TA23 | Analysis | CONFIRM INDEPENDENTLY | The Hann-grid math in the revised task is correct. | Independent Python standard-library summation gave bin spacing 585.9375 Hz, nearest bins +49,804.6875 and -75,000 Hz, periodic Hann ENBW 1.5000000000000029 bins, L(1/3)=-0.6269092766247888 dB and predicted relative peak level -5.373090723375212 dB. | independent calculation 2026-11-20 | This verifies the stated mathematical model only, not the archived I/Q bytes or any hardware observation. |
| TA24 | Governance | REJECT INFERENCE | Reference broadcast or synthetic validation proves the target NFMI system. | A synthetic test validates selected software behavior. A public-FM capture can exercise one receiver configuration. Neither establishes device presence, a device-specific carrier, protocol identity, telemetry content, neural decoding or a source of symptoms. | task boundary;independent measurement reasoning | Report synthetic, reference broadcast and device-specific evidence as separate records; keep the latter unmeasured unless an authorized measurement is actually available. |
| TA25 | Data integrity | QUALIFY | Two-file hashes prove authentic capture provenance. | A manifest detects byte changes relative to its recorded digest values. It does not itself prove who made a capture, when, what hardware generated it, or whether the original metadata was true; a mutable manifest can be replaced along with the files. | independent integrity analysis | Preserve manifest custody, acquisition logs, original version and authenticated timestamp/signature where required; use byte-integrity rather than authenticity language. |

## Source register

| ID | Primary source | Access and evidence |
|---|---|---|
| T01 | [Nooelec SMArt v5 product](https://www.nooelec.com/store/sdr/nesdr-smart.html) | opened. 100 kHz–1.75 GHz; direct sampling below 25 MHz; R820T2/R860 in detailed specifications.  |
| T02 | [Nooelec SMArt series support](https://support.nooelec.com/hc/en-us/articles/360005807694-NESDR-SMArt-Series) | opened. Table identifies SMArt v5 R820T2, XTR E4000, XTR lower bound 55 MHz; always-on bias tee for Tee variants.  |
| T03 | [Nooelec SMArTee XTR product](https://www.nooelec.com/store/sdr/sdr-receivers/nesdr-smartee-xtr-sdr.html) | opened. Product narrative gives approximately 65 MHz; technical table gives 55 MHz. Same page internally inconsistent.  |
| T04 | [Nooelec Ham It Up support](https://support.nooelec.com/hc/en-us/articles/360005812474-Ham-It-Up-Upconverter) | opened. 125 MHz local oscillator; software display offset -125 MHz.  |
| T05 | [RTL-SDR V4 end-of-line announcement](https://www.rtl-sdr.com/rtl-sdr-blog-v4-end-of-line/) | opened. 14 May 2026 announcement says original V4 released August 2023, R828D.  |
| T06 | [RTL-SDR V4L launch](https://www.rtl-sdr.com/rtl-sdr-blog-v4l-lite-now-available-for-purchase/) | opened. 11 August 2026; R828S; built-in HF upconverter; diplexed rather than V4 triplexed filtering.  |
| T07 | [RTL-SDR V4L user guide](https://www.rtl-sdr.com/V4L/) | opened. Updated compatible driver required; no signal may result without it.  |
| T08 | [RTL-SDR Blog Windows driver releases](https://github.com/rtlsdrblog/rtl-sdr-blog/releases) | opened/find. V1.4.0 adds V4L support; V4 R828D vs V4L R828S.  |
| T09 | [SDRplay RSP1B datasheet, Jan 2024 v1.0](https://sdrplay.com/wp-content/uploads/2026/06/RSP1B_Datasheet.pdf) | opened PDF/text. 1 kHz–2 GHz; 2–10.66 MS/s; 14 bits through 6.048 MS/s, decreasing resolution at higher rates.  |
| T10 | [SDRplay RSPdx launch press release](https://www.sdrplay.com/resources/RSPdxPressRelease.pdf) | indexed primary PDF; direct open returned 404. 1 November 2019; 1 kHz–2 GHz; up to 10 MHz visibility; 14-bit architecture.  |
| T11 | [RIGOL 1000Z product/model table](https://www.rigolna.com/products/digital-oscilloscopes/1000z/) | opened/find. DS1054Z is listed as 50 MHz, four channels.  |
| T12 | [Tektronix oscilloscope bandwidth and sampling primer](https://www.tek.com/en/documents/primer/evaluating-oscilloscopes) | opened/find. Rise-time/bandwidth coefficient roughly 0.35–0.45; sample rate separately controls temporal detail.  |
| T13 | [SDR++ release channel](https://github.com/AlexandreRouma/SDRPlusPlus/releases) | opened/find. 1.3.2 nightly updated on master commits; source archive explicitly not synchronized.  |
| T14 | [Gqrx v2.17.7 release](https://github.com/gqrx-sdr/gqrx/releases/tag/v2.17.7) | opened. Adds remote I/Q recording start/stop, fixes ARM Mac DMG launch.  |
| T15 | [Python 3.12.14 release](https://www.python.org/downloads/release/python-31214/) | opened. 12 August 2026 release, superseded by 3.12.16.  |
| T16 | [NumPy 2.3.5 release notes](https://numpy.org/doc/stable/release/2.3.5-notes.html) | opened. Supports Python 3.11–3.14; exists as an official release.  |
| T17 | [NumPy 2.5.5 release notes](https://numpy.org/devdocs/release/2.5.5-notes.html) | opened. Released 15 November 2026; Python 3.12–3.15.  |
| T18 | [Pillow 13.0.0 release notes](https://pillow.readthedocs.io/en/stable/releasenotes/13.0.0.html) | opened. Released 16 October 2026.  |
| T19 | [SigMF specification v1.2.6](https://sigmf.org/) | opened/find. Datatype, complex I-first storage, core:sha512, compliance sections.  |
| T20 | [Analog Devices MAX32570 EMV 3.0 application note](https://www.analog.com/en/resources/app-notes/max32570-contactless-pcd-application-noteemv-30-level-1-analog.html) | opened/find. Finite circular-loop field; mutual coupling, loading and detuning effects. NFC comparator only.  |
| T21 | [NXP antenna development reference](https://community.nxp.com/t5/NXP-Designs-Knowledge-Base/Design-your-NFC-Antenna-with-NXP-s-OM29263ADK-development-kit/ta-p/1122234) | opened. Coupling depends on antenna size, orientation, distance and medium.  |
| T22 | [Tektronix ABCs of probes](https://www.tek.com/en/documents/whitepaper/abcs-probes-primer) | opened/find. Real probes/transducers load the source; system bandwidth and loading must be considered.  |
| T23 | [Physics Illinois circular-loop lecture](https://courses.physics.illinois.edu/phys212/su2012/Lectures/Lect14.pdf) | opened PDF/text. On-axis circular-loop field formula; used alongside independent derivation.  |
| T24 | [SDRplay hardware API](https://sdrplay.com/hardware-api/) | opened. Common API for named RSP devices, hardware details should remain model-specific.  |

## Limitations

- RSPdx detailed historical datasheet and launch press-release URLs returned 404 on direct open; the launch remains available through the search index. Detailed rate table is not primary-verified in this audit.
- Legacy SigMF v1.0.0 source fetch was blocked; no claim is made that core:hash was ever valid legacy syntax.
- Hardware was not tested. Subsequent offline software execution is documented in research/offline_validation.md with 27 harness checks and four schema checks/controls.
- SDR++ nightly pages mutate, so current content is not a fixed historical release snapshot.

## Delivery validation rubric

| Criterion | Result |
|---|---|
| Claim-level traceability | Each register row identifies sources or an explicit independent derivation. |
| Temporal precision | Release dates distinguish V4 from V4L; nightly mutability is disclosed. |
| Numerical reproducibility | Standard-library Hann calculation independently reproduced all theoretical values listed above. |
| Measurement scope | No unperformed hardware or clinical validation is presented as completed. |
| Completeness | All assigned claim families are covered; blocked historical schema and RSPdx-detail retrieval are explicit gaps. |



## Execution addendum: TA26 — provenance labels

The offline follow-up found that a nonempty, non-sentinel `center_frequency_source` label enables an absolute axis; it is not externally verified. A synthetic-data control with arbitrary source text produced `rf_absolute_hz` while retaining `NO_LIVE_CAPTURE`. Describe that axis as inherited from declared metadata. See `research/offline_validation.md` and `validation/reexecuted/audit_results.json` controls 26 and 26b.


---

## Appendix E Literature and regulatory transfer

# Literature transfer and regulatory currency audit

Review cutoff: **20 November 2026**. Ten records audited; eight web/primary-source records, one supplied textbook excerpt, one missing image. Publication versions, test setting and measurement domain are kept separate.

## Required refinements

- Update FDA cybersecurity guidance from June 2025 to **February 3, 2026**, based on the current PDF cover. Preserve the February 2 date displayed on FDA's topic page as a metadata discrepancy.
- Attribute **32.3 dB SPL** to the 2024 UmboMic apparatus and **32.4 dB SPL** to the 2026 study. Both concern cadaveric microphone testing, not living-human performance or RF noise measurements.
- Retain the TICI study's **six adults / 52 weeks**, and Card's **one participant / four arrays / 256 electrodes**, with their distinct clinical objectives and recording requirements.
- Describe Doğan/Külah as an analytical wireless-power design study. The AUDITORY item is a documentation request, not an RF characterization study.
- Replace the weak 49 MHz citation with FDA-hosted, model-specific AB labeling where applicable. It also documents **10.7 MHz FM back telemetry**, so reverse telemetry cannot be generalized as load modulation.

These changes improve the source hierarchy, correct version drift and numerical conflation, and keep each result within the system actually studied. No medical diagnosis, individual device attribution or live RF test is established.

## Evidence register

### L01 — The UmboMic: A PVDF Cantilever Microphone

**Yeiser et al.. 2024-07-18 online; August 2024 issue.** DOI: [10.1088/1361-6439/ad5c6d](https://doi.org/10.1088/1361-6439/ad5c6d).

Prototype PVDF cantilever microphone with low-noise charge amplifier tested in fresh cadaveric human temporal bones. Equivalent input noise 32.3 dB SPL over 100 Hz–7 kHz.

**Refinement:** Retain 32.3 dB SPL for this 2024 apparatus only. It is acoustic input-referred noise, not RF received power or spectrum level.

**Transfer limit:** Cadaveric proof of concept; a microphone is not a stimulator, full CI, wireless transmitter or proof of implantation in another person.

**Review depth:** Abstract and publication metadata; initial PMC author manuscript opened, later access challenged. **Classification:** Tier 2: apparatus-specific comparator.

Sources: [1](https://pmc.ncbi.nlm.nih.gov/articles/PMC11529819/) · [2](https://pubmed.ncbi.nlm.nih.gov/39493505/).

Source references: turn467439325view0; turn851246040search0.

### L02 — The UmboMic: Characterization and Testing of a Middle Ear Microphone

**Wawrzynek et al.. 2026-03-16 online; June 2026 issue, 27(3):411–425.** DOI: [10.1007/s10162-026-01039-x](https://doi.org/10.1007/s10162-026-01039-x).

Seven individual sensors characterized on the bench and in five human cadaveric ears (one female, four male). Reported equivalent input noise is 32.4 dB SPL over 100 Hz–7 kHz; between-sensor sensitivity differs by less than 6 dB.

**Refinement:** The 2026 value is 32.4, not the 2024 value 32.3. Separate design versions and samples.

**Transfer limit:** Long-term fixation and complete biocompatibility remain development topics in this article; it is not a living-human clinical implantation study.

**Review depth:** Publisher abstract, metadata, data/code link inspected. Subscription full text not accessed. **Classification:** Tier 2: apparatus-specific comparator.

Sources: [1](https://link.springer.com/article/10.1007/s10162-026-01039-x) · [2](https://pubmed.ncbi.nlm.nih.gov/41840300/).

Source references: turn851826742view2; turn467439325view1.

### L03 — Rehabilitation of human hearing with a totally implantable cochlear implant: a feasibility study

**Lefebvre et al.. 2025-01-08; Communications Medicine 5, 10.** DOI: [10.1038/s43856-024-00719-0](https://doi.org/10.1038/s43856-024-00719-0).

Mi2000 single-group, nonrandomized feasibility trial at two centers: six adults, implantation beginning September 2020, 52-week outcomes; within-person comparison with external SONNET processor. Primary endpoint was adverse events. One anticipated serious device effect resolved; no unanticipated serious device effects. Trial NCT04571333.

**Refinement:** Six adults and 52 weeks are supported. Do not state broad safety/effectiveness established; authors use descriptive analysis without inferential statistics because of small n.

**Transfer limit:** Shows a specified investigational internal operating mode. Does not identify an unknown device or provide an expected ambient RF signature. Manufacturer-held telemetry outcomes were not reported.

**Review depth:** Primary full-text methods/results inspected on PMC; publisher direct page failed. **Classification:** Tier 2: specified investigational device.

Sources: [1](https://www.nature.com/articles/s43856-024-00719-0) · [2](https://pmc.ncbi.nlm.nih.gov/articles/PMC11711238/).

Source references: turn851246040search3; turn851826742view1.

### L04 — An Accurate and Rapidly Calibrating Speech Neuroprosthesis

**Card et al.. 2024-08-14 online; August 15 issue, NEJM 391:609–618.** DOI: [10.1056/NEJMoa2314132](https://doi.org/10.1056/NEJMoa2314132).

One 45-year-old participant with ALS and severe dysarthria; four 64-electrode arrays (256 intracortical electrodes) in left ventral precentral gyrus. Decoder trained on recorded cortical activity during attempted speech; output text and synthesized speech. BrainGate2 NCT00912041.

**Refinement:** 256 electrodes is supported. Preserve invasive recording, participant-specific training and single-participant context.

**Transfer limit:** An RF spectrum or FM recording does not supply the cortical inputs studied here. This paper establishes no ear-local speech decoder or ambient remote decoding method.

**Review depth:** PubMed primary abstract and figure legends inspected; NEJM 403, PMC CAPTCHA; full methods not reviewed. **Classification:** Tier 2: specified participant and apparatus.

Sources: [1](https://www.nejm.org/doi/10.1056/NEJMoa2314132) · [2](https://pubmed.ncbi.nlm.nih.gov/39141853/).

Source references: turn851246040search4; turn633814248view1.

### L05 — Physics-based design space analysis for inductive wireless power transfer in cochlear implants

**Mert Doğan and Haluk Külah. 2026-09-15.** DOI: [10.1038/s41598-026-69074-5](https://doi.org/10.1038/s41598-026-69074-5).

A 12-coil analytical design library calibrated against Maxwell 2D simulations evaluates 6.78, 13.56 and 27.12 MHz at 3–20 mm model implant depth; charging-scenario analysis includes phantom-validated thermal scaling.

**Refinement:** 13.56 MHz is one modeled ISM-band design point, not a survey establishing a commercial implant's carrier. Publisher listing labels it early accepted research awaiting final version.

**Transfer limit:** Simulation, phantom scaling, and design optimization are not human clinical measurements. No performance number transfers to an unspecified coil, device, tissue or operating condition.

**Review depth:** Primary-domain indexed abstract and publication metadata retrieved. Direct article access failed at publisher identity redirect; full text not inspected. **Classification:** Tier 2: modeled design space.

Sources: [1](https://www.nature.com/articles/s41598-026-69074-5).

Source references: turn851246040search5; turn547627546search0.

### L06 — RF Tx Frequencies used by CI Processors and Interference

**Sharath Chandra Ramakrishnan. 2025-01-15 01:16:49 -0600.** 

The author states 49 MHz for some AB processors, naming Harmony and Neptune, while requesting technical documentation and interference studies.

**Refinement:** Classify as a lead, not a measured or independently verified carrier specification, and not a study demonstrating interference.

**Transfer limit:** Questions in a mailing list do not establish exposure, vulnerability, interference occurrence or individual causation. Use model-specific primary labeling instead.

**Review depth:** Original full posting inspected. **Classification:** Tier 2 lead only; do not promote to established measurement.

Sources: [1](https://www.auditory.org/postings/2025/22.html).

Source references: turn547627546view2.

### L07 — Cybersecurity in Medical Devices: Quality Management System Considerations and Content of Premarket Submissions

**U.S. FDA, CDRH and CBER. 2026-02-03 per guidance cover and HHS record.** 

Final guidance, docket FDA-2021-D-1158, supersedes June 27, 2025 guidance. February 2026 changes align with QMSR amendments. Guidance addresses cybersecurity design, labeling, submission documentation, and FD&C Act section 524B for cyber devices.

**Refinement:** Replace 'June 2025 current guidance' with February 2026 current guidance; retain 2025 only as historical predecessor. FDA topic page says February 2 but PDF cover/HHS say February 3; cite PDF issue date and preserve discrepancy.

**Transfer limit:** Nonbinding guidance recommendations are distinct from statutory requirements. Premarket cybersecurity guidance does not authorize personal device testing or establish an incident.

**Review depth:** Official guidance cover, scope overview and revision history; official landing page and HHS metadata inspected. **Classification:** Governance authority; scientific measurement tiers not applicable.

Sources: [1](https://www.fda.gov/media/119933/download) · [2](https://www.fda.gov/regulatory-information/search-fda-guidance-documents/cybersecurity-medical-devices-quality-management-system-considerations-and-content-premarket) · [3](https://www.fda.gov/medical-devices/medical-device-cybersecurity) · [4](https://www.hhs.gov/guidance/document/cybersecurity-medical-devices-quality-management-system-considerations-and-content).

Source references: turn547627546view1; turn547627546view0; turn633814248view3; turn633814248view4.

### L08 — Advanced Bionics HiRes Ultra / HiRes Ultra 3D labeling, PMA P960058/S167

**Advanced Bionics; FDA-hosted approved labeling. Supplement approval 2026-07-22 per SSED.** 

Named HiRes Ultra/Ultra3D labeling specifies 49 MHz inductive power/forward link, 1.11 Mbit/s OOK or ASK, and intermittently keyed 10.7 MHz FM back telemetry. SSED identifies Ultra/Ultra3D and Naida Q/M systems and says indication expansion required no design changes.

**Refinement:** Stronger source than the AUDITORY post. 49 MHz is not restricted to a legacy historical anecdote. Do not characterize all reverse telemetry as load modulation: these named models specify a separate FM transmitter.

**Transfer limit:** Manufacturer specifications apply only to those labeled models and configurations. They neither identify a signal in an SDR recording nor establish any person's device status.

**Review depth:** Wireless-communication sections and SSED model/approval pages inspected; no device or RF measurements performed. **Classification:** Tier 1 for verified published model specification; Tier 2 for transfer to a new physical target.

Sources: [1](https://www.accessdata.fda.gov/cdrh_docs/pdf/P960058S167D.pdf) · [2](https://www.accessdata.fda.gov/cdrh_docs/pdf/P960058S167B.pdf).

Source references: turn991011010view0; turn991011010view1.

### L09 — Programming Cochlear Implants, third edition — supplied excerpt

**Jace Wolfe and Erin C. Schafer. Copyright 2026; ISBN 9781635501766.** 

22-page supplied PDF includes front matter/contents and chapter 1 printed pp.1–6. Pages 2–4 describe external sound processing, inductive RF power/data and internal stimulation. Pages 5–6 explain typical approximate acoustic/electrical dynamic ranges and manufacturer-dependent threshold definitions.

**Refinement:** The contents list RF and telemetry on printed page 25, but that page is absent. Do not imply the complete textbook or its RF chapter was reviewed. Dynamic-range examples are explanatory, not measured values for a target.

**Transfer limit:** Clinical terminology supports architecture description, not RF signature attribution, programming instructions or device diagnosis.

**Review depth:** Library extracted text inspected for title/copyright/contents and printed pp.1–6; illustrations not visually audited. **Classification:** Background architecture/terminology only.



Source references: Library:libfile_fde3_f-3d8bcd386ed88191a33738ce6751bcf2_537c53a806188191a8b4bdb9819ba1f7.

### L10 — PNG.png conceptual governance diagram

**Unverified. Date unverified.** 

No image was available for independent inspection in this audit.

**Refinement:** Mark missing/unverified. Parent reports exact-title and broader searches failed; textual descriptions in the task are not a substitute for the image.

**Transfer limit:** Do not report image features, gates or clinical claims as independently verified.

**Review depth:** No image inspected. **Classification:** Unverified source.



Source references: None; source missing.

## Assumptions, validation and quality rubric

Assumption: this is a literature/archival audit, with no new clinical or RF measurements. Criteria: primary source supports each number; populations and domains are explicit; current guidance supersession is checked; missing sources and incomplete access remain visible. Validation completed: publication identity and core sample/measurement details cross-checked; supplied textbook contents bounded to actual excerpt; major source substitutions identified. Quality: traceability—met; currency—met for retrieved FDA guidance; numeric consistency—met; complete full-text review—partial; individual clinical inference—none.

**Remaining access limits:** Wawrzynek full text is subscription content; Card full text was blocked although the author abstract and figure legends were available; Doğan/Külah direct full text failed at a publisher redirect. Do not describe these as complete full-text systematic reviews. The 2026 UmboMic publisher page supplies a data/code link, but its dataset was not downloaded or reanalyzed.



---

## Appendix F Study correction register

# Corpus patch register — proposed corrections and retained qualifications

20 November 2026. Original files were read and hashed; no source HTML was modified. Forty section-specific dispositions distinguish defects in the two early drafts from qualifications already present in the revised manual and methods.

## How to use this register

Use the filename, HTML anchor/section and original HTML line together. Apply changes to a new corrected edition or companion, preserving historical originals. Code edits require synchronized visible listings, copy-button payloads, embedded downloads and manifests. RETAIN entries document accurate existing text, not defects.

Assumption: archival/offline review only. Acceptance criteria: each excerpt locates in its named file; each correction maps to a source/audit record; unknown evidence remains unknown; original hashes remain unchanged.

Validation: all 40 excerpts were located; four source files were fingerprinted; each original draft contains one malformed ShmooCon URL, while each revised file contains the canonical URL. The early supplement contains 45 unresolved reference tokens.

Severity counts: Medium: 12, High: 17, Critical: 4, Low: 2, None: 5.

## Source fingerprints

| Source file | Bytes | SHA-256 |
|---|---:|---|
| Supplemetal_RF Characterization CI NFMI Link.html | 39,336 | `1fe4d6c42abb5588a7ad3552f4120182c54e1f155a67c81158c3f59f39e778ba` |
| RF Characterization CI NFMI Link.html | 58,683 | `aac9747be6fe43f67717e51a158986eaf33bfe8262e0c6648d43ab7805307250` |
| RF_Measurement_Supplementary_Methods.html | 8,274,465 | `f563125ef843236d1819ba7a7c4301756de604908d8e38d0dd216e50c214a3b4` |
| RF_Measurement_Field_Manual.html | 8,866,313 | `6d381632564bfa53f1954b51e78555eda426ba1b7003894e496459d24a1a5505` |

## Supplemetal_RF Characterization CI NFMI Link.html

### CP02 — #s6 / Reference 1

**Medium; REPLACE_HREF.** Original HTML line 459.

Current excerpt: “shmooocon-xiii”

**Proposed wording / disposition:** https://infocondb.org/con/shmoocon/shmoocon-xiii/cyborg-self-hacking-an-examination-of-cochlear-implants

**Why:** One defective link occurs here; the revised manual and revised methods each already use the canonical URL.

**Evidence:** A-focal.

Sources: [source 1](https://infocondb.org/con/shmoocon/shmoocon-xiii/cyborg-self-hacking-an-examination-of-cochlear-implants) · [source 2](https://web.archive.org/web/20170118065535/http://shmoocon.org/speakers/) · [source 3](https://www.youtube.com/watch?v=ihcaNoUJ6BU).
### CP05 — #s1-4 / receive chain

**High; REPLACE.** Original HTML line 145.

Current excerpt: “≥20 MS/s, ≥100 MHz analog bandwidth”

**Proposed wording / disposition:** Select bandwidth, sample rate and probe loading for the defined measurand. Direct real sampling of a 49 MHz carrier requires more than 98 MS/s before practical margin unless a separately justified bandpass-sampling scheme is used. Envelope-edge measurements require their own rise-time and filter analysis. No single rate/bandwidth pair is universally sufficient.

**Why:** The fixed minima conflate RF-carrier sampling, envelope sampling and edge fidelity.

**Evidence:** TA08, TA09, TA10, TA18.

Sources: [source 1](https://www.rigolna.com/products/digital-oscilloscopes/1000z/) · [source 2](https://www.tek.com/en/documents/primer/evaluating-oscilloscopes) · [source 3](https://www.analog.com/en/resources/app-notes/max32570-contactless-pcd-application-noteemv-30-level-1-analog.html) · [source 4](https://community.nxp.com/t5/NXP-Designs-Knowledge-Base/Design-your-NFC-Antenna-with-NXP-s-OM29263ADK-development-kit/ta-p/1122234) · [source 5](https://www.tek.com/en/documents/whitepaper/abcs-probes-primer).
### CP08 — #s1-4 / antenna

**High; REPLACE.** Original HTML line 145.

Current excerpt: “The antenna is a small multi-turn”

**Proposed wording / disposition:** For a separately authorized bench fixture, choose and characterize the probe for the intended frequency response, electric/magnetic selectivity, aperture, orientation and loading. More turns or a ferrite core are not universally preferable. No patient-adjacent pickup was performed here.

**Why:** A universal probe prescription lacks a transfer function and loading assessment.

**Evidence:** TA17, TA18.

Sources: [source 1](https://www.analog.com/en/resources/app-notes/max32570-contactless-pcd-application-noteemv-30-level-1-analog.html) · [source 2](https://www.tek.com/en/documents/whitepaper/abcs-probes-primer) · [source 3](https://community.nxp.com/t5/NXP-Designs-Knowledge-Base/Design-your-NFC-Antenna-with-NXP-s-OM29263ADK-development-kit/ta-p/1122234).
### CP10 — #s1-5 / metadata

**High; REPLACE.** Original HTML line 156.

Current excerpt: “Required fields are”

**Proposed wording / disposition:** Use a versioned SigMF schema and separately list study-required provenance. Core datatype/version, capture indices and other fields must satisfy their defined scopes and types. Unknown optional numeric/time fields are omitted; unresolved acquisition information remains explicit in a documented application sidecar. Complex core samples are I then Q.

**Why:** The current paragraph mixes scientific reporting requirements with standard-required fields and permits invalid sentinels.

**Evidence:** TA19, TA20, TA21, TA22.

Sources: [source 1](https://sigmf.org/).
### CP11 — #s2-4 / example sidecar

**High; SUPERSEDE_EXAMPLE.** Original HTML line 361.

Current excerpt: “core:hash”

**Proposed wording / disposition:** Use global core:sha512 with the computed unprefixed 128-hex-character dataset digest. Remove the illustrative sha512:... value. Set core:version to the specification actually validated; the revised example targets 1.2.6. Do not assert that core:hash was valid in v1.0.0.

**Why:** The original example is not an executable valid digest; legacy migration language was not verified.

**Evidence:** TA19, TA21, V:#controls.

Sources: [source 1](https://sigmf.org/).
### CP12 — #s2-4 / annotation sample_count

**Medium; CLARIFY.** Original HTML line 373.

Current excerpt: “2400000”

**Proposed wording / disposition:** State explicitly that an annotation of 2,400,000 complex samples covers 1 second at 2.4 MS/s. It is valid within a longer recording if that is the intended interval. Set annotation length from its intended scope and validate bounds against the actual dataset.

**Why:** The one-second annotation is not inherently invalid merely because acquisition guidance says 5–10 seconds.

**Evidence:** TA21, M:#addendum.

Sources: [source 1](https://sigmf.org/).
### CP14 — #s2-1 / analyze_iq.py

**High; SUPERSEDE_CODE.** Original HTML line 208.

Current excerpt: “np.fromfile(path, dtype=np.complex64)”

**Proposed wording / disposition:** Mark this as the original draft analyzer, superseded for reproducible runs by the preserved rf_reference.py version and its manifest. Document raw datatype/endian handling, WAVE domain routing, input validation, estimator normalization and actual tested environment.

**Why:** The supplied code does not implement the prose's audio-file route and is not the revised analyzer.

**Evidence:** TA20, TA21, M:#analyze, V:#estimator.

Sources: [source 1](https://sigmf.org/).
### CP16 — #s1-7 / estimator description

**High; REPLACE.** Original HTML line 166.

Current excerpt: “waterfall with an absolute RF frequency axis”

**Proposed wording / disposition:** The historical listing uses a symmetric NumPy Hann window and a baseband waterfall. The revised kit explicitly uses a periodic Hann window, averages normalized linear power density, and chooses absolute RF, offset or audio axes from provenance. Report these as different implementations.

**Why:** The periodic-Hann result cannot silently be attributed to the original symmetric-window listing.

**Evidence:** TA23, M:#analyze, V:#estimator.
### CP17 — #s2-3 / validate_peaks.py

**High; SUPERSEDE_CODE.** Original HTML line 326.

Current excerpt: “def peak_near”

**Proposed wording / disposition:** Retain the draft validator for audit history. For accepted results, run the revised analyzer on the preserved asymmetric fixture, find separated peaks over the full band before scoring signs, use the same mean spectrum as production analysis, and require a nonzero process exit code on failure. Verify this with negative controls.

**Why:** Expected-frequency neighborhood searches preselect signs, one frame differs from the main average, and the old script only prints FAIL.

**Evidence:** TA23, V:#controls, M:#addendum.
### CP18 — #s3-3 / synthetic validation table

**Critical; REPLACE_WITH_AUDITED_RECORD.** Original HTML line 411.

Current excerpt: “+50,012 Hz; −74,988 Hz”

**Proposed wording / disposition:** Withdraw these entries as unsupported by the displayed uninterpolated FFT algorithm. At 2.4 MS/s and NFFT 4096, grid spacing is 585.9375 Hz; the expected nearest bins for the specified tones are +49,804.6875 Hz and -75,000 Hz. Present revised deterministic fixture measurements under a new dataset ID, with hashes and estimator details.

**Why:** Neither original frequency is an FFT-grid point. Do not rewrite them as though they were newly recovered original observations.

**Evidence:** TA23, V:#results, V:#controls.
### CP19 — #s3-3 / level and claimed run provenance

**Critical; REPLACE_WITH_QUALIFIED_FINDING.** Original HTML line 413.

Current excerpt: “5.97 dB”

**Proposed wording / disposition:** The original waveform bytes, random seed and complete run record were not supplied; the claimed 5.97 dB observation cannot be independently verified. For the revised periodic-Hann noise-free fixture, distinguish the -6 dB encoded amplitude ratio from the predicted -5.373090723 dB weak-minus-strong peak-bin ratio.

**Why:** Window choice, grid location and stochastic waveform differ; exact revised values are not evidence for the old run.

**Evidence:** TA23, V:#results, V:#controls.
### CP20 — #s2-2 / synthetic generator

**Medium; REPLACE_METHOD_NOTE.** Original HTML line 301.

Current excerpt: “np.random.randn”

**Proposed wording / disposition:** For repeatable numerical reference use the archived deterministic fixtures and their hashes. If retaining a noisy simulation, specify RNG algorithm and seed, library/runtime, datatype byte order and waveform digest. Label it a separate stochastic test rather than the source of the revised noise-free result.

**Why:** The source has unseeded noise and native complex64 output, preventing exact regeneration from the printed metadata.

**Evidence:** V:#design, V:#controls.
### CP23 — #s1-5 / FM reference

**High; REPLACE.** Original HTML line 153.

Current excerpt: “catches frequency-axis, FFT-scaling, and waterfall-time-axis errors”

**Proposed wording / disposition:** Use the public broadcast as a documented functional receiver check, reported separately from software fixtures. Independently validate scaling and timebase where accuracy is claimed; the strongest FM spectral bin is not an absolute calibration reference.

**Why:** A recognizable spectrum and published station allocation do not prove all numerical scales.

**Evidence:** TA24, V:#receiver.
### CP25 — #s1-8 and #s6 / URH and fork

**High; REPLACE.** Original HTML line 171.

Current excerpt: “URH-NG AI fork”

**Proposed wording / disposition:** Use an exact validated tool version for offline analysis. The original URH repository is archived; its cited paper credits Johannes Pohl and Andreas Noack. Any AI-assisted fork remains an unvalidated optional comparator until its source, version and performance are independently checked. Do not claim a custom final Manchester decoder ran without its code and logs.

**Why:** The source describes tools and an absent custom decoder as used; this review verified project provenance, not execution or fork accuracy.

**Evidence:** C-T01, C-T02.

Sources: [source 1](https://github.com/jopohl/urh) · [source 2](https://github.com/jopohl/urh/releases) · [source 3](https://www.usenix.org/conference/woot18/presentation/pohl) · [source 4](https://github.com/miek/inspectrum).
### CP26 — #s4-1 / historical device findings

**High; REPLACE.** Original HTML line 424.

Current excerpt: “Those findings were accurate for that device and that generation.”

**Proposed wording / disposition:** These are speaker-reported interpretations from the historical presentation. The available automatic transcript describes unfinished interpretation and future reverse-telemetry work. Exact packet units, NVRAM behavior and security properties require original audio/slide confirmation and device documentation before specification-level use.

**Why:** A historical assertion is not independently verified truth; packet-size units are uncertain in captions.

**Evidence:** A-focal.

Sources: [source 1](https://infocondb.org/con/shmoocon/shmoocon-xiii/cyborg-self-hacking-an-examination-of-cochlear-implants) · [source 2](https://web.archive.org/web/20170118065535/http://shmoocon.org/speakers/) · [source 3](https://www.youtube.com/watch?v=ihcaNoUJ6BU).
### CP27 — #s5 / Code and Data availability

**Critical; REPLACE.** Original HTML line 448.

Current excerpt: “github.com/example/ci-nfmi-receive-only”

**Proposed wording / disposition:** No resolvable repository accession or dataset DOI was supplied for the original draft. The repository address is a placeholder. The revised synthetic fixtures, scripts and checksums are available in the named delivered kit; no live FM or implant-link recording was supplied. Add a public accession only after depositing and checking the exact version.

**Why:** The following paragraph asserts deposited FAIR data and a DOI without providing either. Preserve the source; do not represent those deposits as verified.

**Evidence:** V:#data, CORPUS.
### CP28 — header, status and footer

**Critical; REPLACE.** Original HTML line 83.

Current excerpt: “Post-editor-review revision”

**Proposed wording / disposition:** Draft supplementary methods with an independent source and numerical audit. No journal acceptance, completed external peer review or editorial approval is established by the supplied records. Submission readiness remains contingent on resolving the provenance, citation and validation issues listed in the companion.

**Why:** Self-description as post-editor-review/submission-ready is unsupported by any review record supplied here.

**Evidence:** CORPUS.
### CP29 — throughout / unresolved reference tokens

**High; RESOLVE_REFERENCES.** Original HTML line 121.

Current excerpt: “[reference:0]”

**Proposed wording / disposition:** Replace each [reference:n] token with an explicit resolvable citation that supports the adjacent claim; keep the bibliographic label and the reference target in one checked register. Until resolved, mark the claim's source as unresolved rather than treating the numbered token as evidence.

**Why:** 45 unresolved tokens occur; n ranges from 0 to 44 while the visible bibliography has ten entries. No mapping is supplied.

**Evidence:** CORPUS.
### CP30 — #s4-2 / scope and authorization statement

**Medium; REPLACE_SCOPE_LANGUAGE.** Original HTML line 429.

Current excerpt: “active transmission to an implanted medical device is not a research method”

**Proposed wording / disposition:** This task authorizes no active transmission, replay, jamming, device modification or patient-connected probing. Its receive-only/archival scope is a task boundary, not a claim that every separately authorized medical-device research intervention is unlawful.

**Why:** The original sentence makes a categorical research/legal statement that does not follow from the cited guidance.

**Evidence:** CORPUS.

## RF Characterization CI NFMI Link.html

### CP01 — #links / Background

**Medium; REPLACE_HREF.** Original HTML line 1006.

Current excerpt: “shmooocon-xiii”

**Proposed wording / disposition:** https://infocondb.org/con/shmoocon/shmoocon-xiii/cyborg-self-hacking-an-examination-of-cochlear-implants

**Why:** The original URL has one extra o. Preserve the source and use the canonical URL in the corrected companion.

**Evidence:** A-focal.

Sources: [source 1](https://infocondb.org/con/shmoocon/shmoocon-xiii/cyborg-self-hacking-an-examination-of-cochlear-implants) · [source 2](https://web.archive.org/web/20170118065535/http://shmoocon.org/speakers/) · [source 3](https://www.youtube.com/watch?v=ihcaNoUJ6BU).
### CP03 — #changes / Waveform capture / 2017 baseline

**Medium; REPLACE.** Original HTML line 183.

Current excerpt: “Analog oscilloscope + hand-wound loop”

**Proposed wording / disposition:** Digital oscilloscope (Rigol DS1054Z, as identified in the supplied historical exhibit) and an inductive pickup loop. Attribute the setup to the historical source; it was not reproduced in this review.

**Why:** The named model is a digital scope and is specified at 50 MHz; the old description calls it analog.

**Evidence:** A-focal, TA08, M:#transfer.

Sources: [source 1](https://infocondb.org/con/shmoocon/shmoocon-xiii/cyborg-self-hacking-an-examination-of-cochlear-implants) · [source 2](https://web.archive.org/web/20170118065535/http://shmoocon.org/speakers/) · [source 3](https://www.youtube.com/watch?v=ihcaNoUJ6BU) · [source 4](https://www.rigolna.com/products/digital-oscilloscopes/1000z/).
### CP04 — #changes and #phase2 / discovery receiver

**High; REPLACE.** Original HTML line 178.

Current excerpt: “add Ham It Up upconverter for <30 MHz”

**Proposed wording / disposition:** Record the exact receiver and operating mode. Official XTR material gives conflicting approximately 55/65 MHz lower limits; both exclude 49 MHz and 13.56 MHz. For an appropriate upconverter, record its +125 MHz mixing LO and -125 MHz display correction separately. Do not use a <30 MHz-only rule for the XTR.

**Why:** The original rule can leave 30–55/65 MHz uncovered, including the stated historical 49 MHz feature.

**Evidence:** TA02, TA03.

Sources: [source 1](https://support.nooelec.com/hc/en-us/articles/360005807694-NESDR-SMArt-Series) · [source 2](https://www.nooelec.com/store/sdr/sdr-receivers/nesdr-smartee-xtr-sdr.html) · [source 3](https://support.nooelec.com/hc/en-us/articles/360005812474-Ham-It-Up-Upconverter).
### CP06 — #phase2 / Phase 2.2

**High; REPLACE.** Original HTML line 362.

Current excerpt: “at least 20 MS/s”

**Proposed wording / disposition:** For an authorized bench measurement, distinguish direct-RF and envelope inputs; derive rate, analog bandwidth and probe requirements from the fastest feature and tolerated error. The historical DS1054Z model does not establish a universal minimum.

**Why:** 20 MS/s is not a universal scope-grade edge or 49 MHz carrier specification.

**Evidence:** TA08, TA09, TA10.

Sources: [source 1](https://www.rigolna.com/products/digital-oscilloscopes/1000z/) · [source 2](https://www.tek.com/en/documents/primer/evaluating-oscilloscopes).
### CP07 — #phase1 / Phase 1.1

**High; REPLACE.** Original HTML line 282.

Current excerpt: “held against the head”

**Proposed wording / disposition:** The historical account describes a pickup near the presenter's known system. This document transfers only the measurement reasoning. Physical coupling to a patient-connected device is outside the executed workflow; receive-only equipment can still load or detune a resonant link.

**Why:** The sentence converts a historical action into a current prescription and overstates noninteraction.

**Evidence:** TA16, TA17, TA18, A-focal.

Sources: [source 1](https://www.analog.com/en/resources/app-notes/max32570-contactless-pcd-application-noteemv-30-level-1-analog.html) · [source 2](https://courses.physics.illinois.edu/phys212/su2012/Lectures/Lect14.pdf) · [source 3](https://www.tek.com/en/documents/whitepaper/abcs-probes-primer) · [source 4](https://community.nxp.com/t5/NXP-Designs-Knowledge-Base/Design-your-NFC-Antenna-with-NXP-s-OM29263ADK-development-kit/ta-p/1122234) · [source 5](https://infocondb.org/con/shmoocon/shmoocon-xiii/cyborg-self-hacking-an-examination-of-cochlear-implants) · [source 6](https://web.archive.org/web/20170118065535/http://shmoocon.org/speakers/) · [source 7](https://www.youtube.com/watch?v=ihcaNoUJ6BU).
### CP09 — #phase3 / Phase 3.2 checklist and example

**High; REPLACE.** Original HTML line 487.

Current excerpt: “unknown fields are explicitly marked”

**Proposed wording / disposition:** Distinguish this study's acquisition requirements from SigMF's schema requirements. Omit unknown optional typed SigMF fields; retain unresolved provenance in a documented custom field or application sidecar. Core complex SigMF stores I then Q. Preserve original QI exports and document any conversion to canonical I/Q.

**Why:** UNKNOWN in standard numeric/time fields can be invalid; custom QI acceptance is not core SigMF conformance.

**Evidence:** TA19, TA20, TA21, TA22.

Sources: [source 1](https://sigmf.org/).
### CP13 — #phase4 / analyze_iq.py displayed listing and data-copy attribute

**High; SUPERSEDE_CODE.** Original HTML line 640.

Current excerpt: “np.fromfile(path, dtype=np.complex64)”

**Proposed wording / disposition:** Retain this listing as historical draft code and direct executable use to the audited rf_reference.py kit. The replacement reader must distinguish headerless cf32_le/ci16_le/cu8, wav_iq and wav_audio; enforce byte order and complete sample pairs; reject nonfinite/short data; and validate sample rate and metadata.

**Why:** Native-endian raw loading and missing validation do not support all formats claimed in the prose. Update copy-button payloads with any future visible-code edit.

**Evidence:** TA20, TA21, M:#analyze, V:#estimator.

Sources: [source 1](https://sigmf.org/).
### CP15 — #phase4 / opening paragraph and checklist

**Medium; REPLACE.** Original HTML line 534.

Current excerpt: “a waterfall with an absolute RF frequency axis”

**Proposed wording / disposition:** The draft spectrum adds the supplied center to the FFT grid; its waterfall is labeled baseband frequency relative to center. In the corrected workflow, use an absolute RF axis only when I/Q data and independently documented center metadata support it; otherwise show signed offsets or audio frequency.

**Why:** The old prose conflicts with the displayed waterfall code and assumes an always-known RF center.

**Evidence:** TA24, M:#capture, V:#estimator.
### CP21 — #phase5 / synthetic generator, displayed code and data-copy attribute

**Medium; REPLACE_METHOD_NOTE.** Original HTML line 797.

Current excerpt: “np.random.randn”

**Proposed wording / disposition:** Use the preserved deterministic fixture for the reported acceptance result. A separate noisy simulation must record seed/RNG and dtype byte order; any change must update both the displayed listing and copy-button payload.

**Why:** Multiple code copies can diverge, and unseeded noise is not a byte-reproducible fixture.

**Evidence:** V:#design, V:#controls.
### CP22 — #phase3 / Phase 3.1 reference policy

**High; REPLACE.** Original HTML line 381.

Current excerpt: “used to prove that the frequency axis”

**Proposed wording / disposition:** A documented FM capture exercises one receiver/recorder configuration and provides a consistency check. It does not by itself calibrate FFT amplitude, timebase accuracy or a different magnetic pickup chain. A station's strongest bin depends on programme content; use a traceable reference for accuracy calibration.

**Why:** The revised manual already separates a functional receiver check from calibration and NFMI sensitivity.

**Evidence:** TA24, M:#results, M:#addendum.
### CP24 — #changes and #phase4 / URH

**Medium; REPLACE.** Original HTML line 731.

Current excerpt: “Universal Radio Hacker (URH) 2.10.x”

**Proposed wording / disposition:** URH v2.10.0 is a historical release listed by the official project. The official repository was archived on 29 March 2026. Pin the installed version/commit and dependencies, assess any fork independently, and restrict this workflow to saved-file analysis.

**Why:** A version family is not a fixed executable pin or assurance of continuing support.

**Evidence:** C-T01.

Sources: [source 1](https://github.com/jopohl/urh) · [source 2](https://github.com/jopohl/urh/releases) · [source 3](https://www.usenix.org/conference/woot18/presentation/pohl).
### CP31 — #phase0 / Phase 0.2 folder commands

**Low; CORRECT_COMMAND_PATTERN.** Original HTML line 266.

Current excerpt: “$(date -u +%Y-%m-%dT%H%M%SZ)”

**Proposed wording / disposition:** Compute the timestamp once, assign the capture directory to a task-specific variable, then create and enter that same quoted path. Preserve originals and place derivatives in a separate directory.

**Why:** Two separate date invocations may cross a second boundary and select different paths.

**Evidence:** CORPUS.

## RF_Measurement_Supplementary_Methods.html

### CP36 — #controls / Disposition of supplied examples

**None; RETAIN.** Original HTML line 53.

Current excerpt: “Full conformance against the upstream JSON Schema was not tested.”

**Proposed wording / disposition:** Retain this qualification. Any new schema-validation result should name the schema version/hash, validator and semantic checks performed; do not overwrite the historical test statement.

**Why:** The revised methods are already calibrated correctly.

**Evidence:** TA19, TA20, TA21.

Sources: [source 1](https://sigmf.org/).
### CP37 — #receiver / Preserve file identity

**Low; ADD_EXPLICIT_LIMIT.** Original HTML line 76.

Current excerpt: “require both digests to match”

**Proposed wording / disposition:** Require both digests to match the source manifest, and preserve the manifest's custody. This establishes byte agreement with the manifest, not creator identity, acquisition time, physical-source identity or the truth of metadata. An authenticated provenance record is separate.

**Why:** The manual already states this limit; repeating it makes the standalone supplementary protocol self-contained.

**Evidence:** TA25, M:#addendum.
### CP39 — #replay / Windows and macOS reproduction blocks

**Medium; ADD_EXECUTION_GATE.** Original HTML line 59.

Current excerpt: “py -3.12 -m venv .venv”

**Proposed wording / disposition:** Run the environment setup, dependency installation and validation commands sequentially with explicit failure checks. A failed native command must prevent dependent commands; report the exact failed stage and retain its output.

**Why:** Nonzero script exit statuses help only if the enclosing procedure observes them.

**Evidence:** CORPUS.
### CP40 — #replay / cross-host comparison

**None; RETAIN.** Original HTML line 70.

Current excerpt: “font rendering across platforms”

**Proposed wording / disposition:** Retain this limitation: compare raw-input hashes and explicit numerical outputs; rendered file byte identity is a separate test. Pinning Pillow alone does not prove cross-platform pixel identity.

**Why:** The supplied revised source already acknowledges rendering variability; the later task's deterministic-pixel wording overstates it.

**Evidence:** TA15.

Sources: [source 1](https://pillow.readthedocs.io/en/stable/releasenotes/13.0.0.html).

## RF_Measurement_Field_Manual.html

### CP32 — #capture / Make the handoff

**Medium; CLARIFY_SEQUENCE.** Original HTML line 88.

Current excerpt: “Finalize the sidecar and preserve both files”

**Proposed wording / disposition:** On the capture host, close and hash the recording, finalize the sidecar, then create and retain the two-file manifest. Transfer the recording, finalized sidecar and source manifest together. Verify both copied files against that manifest before analysis; preserve earlier versions if metadata changes.

**Why:** Chapter 03's order is ambiguous; chapter 08 already gives the correct finalize-before-manifest-before-transfer sequence.

**Evidence:** TA25, M:#addendum.
### CP33 — #equipment / SDR++ and Gqrx

**None; RETAIN.** Original HTML line 75.

Current excerpt: “SDR++’s nightly label moves with development.”

**Proposed wording / disposition:** Retain this caveat. For a reproducible run, capture the exact build/commit or binary SHA-256 and platform asset. Gqrx 2.17.7 exists, but release existence and local capture success remain separate records.

**Why:** The revised manual already avoids the mutable-nightly error introduced by the later task summary.

**Evidence:** TA11, TA12.

Sources: [source 1](https://github.com/AlexandreRouma/SDRPlusPlus/releases) · [source 2](https://github.com/gqrx-sdr/gqrx/releases/tag/v2.17.7).
### CP34 — #equipment / Scientific Python

**None; RETAIN_WITH_RUN_PROVENANCE.** Original HTML line 77.

Current excerpt: “NumPy 2.5.5 release is a candidate”

**Proposed wording / disposition:** Retain the distinction: the archived kit reports CPython 3.12.14, NumPy 2.3.5 and Pillow 13.0.0; NumPy 2.5.5 is a candidate for a separate compatibility run. Attribute historical execution to archived metadata, and append the actual environment and outcomes of this review separately.

**Why:** All named releases exist. The source does not claim NumPy2.5.5 was already tested; do not misreport it as a fabricated version or completed run.

**Evidence:** TA13, TA14, TA15, V:#materials.

Sources: [source 1](https://www.python.org/downloads/release/python-31214/) · [source 2](https://numpy.org/doc/stable/release/2.3.5-notes.html) · [source 3](https://numpy.org/devdocs/release/2.5.5-notes.html) · [source 4](https://pillow.readthedocs.io/en/stable/releasenotes/13.0.0.html).
### CP35 — #addendum / Reproduce the result

**None; RETAIN.** Original HTML line 280.

Current excerpt: “Full validation against the published JSON Schema remains unverified.”

**Proposed wording / disposition:** Retain this explicit limit unless this execution supplies a separately logged versioned-schema validation plus semantic checks. The example checker validates selected fields and bytes; that is not blanket SigMF conformance.

**Why:** The later task's strict-compliance claim is stronger than the revised manual itself.

**Evidence:** TA21, V:#controls.

Sources: [source 1](https://sigmf.org/).
### CP38 — #analyze / Windows and macOS command blocks

**Medium; ADD_EXECUTION_GATE.** Original HTML line 205.

Current excerpt: “py -3.12 -m venv .venv”

**Proposed wording / disposition:** Before each dependent analysis step, stop if the previous command fails. In PowerShell check $LASTEXITCODE after each native executable; do not rely solely on $ErrorActionPreference. In a POSIX script use explicit status checks or an appropriate fail-fast wrapper. Preserve logs and the completed-command list.

**Why:** The snippets list independent lines but do not implement the task summary's claimed exit-code-gated batch sequence.

**Evidence:** CORPUS.

## Do not project later summary errors into the revised sources

- Combined V4/V4L August2026 launch: revised manual correctly specifies V4L only.
- SMArt v5 fixed 25MHz tuning floor/R828D conflation: not asserted in the revised manual's equipment row.
- Universal RSP1B 14-bit rate claim: revised manual already limits 14 bits to 2–6.048 MS/s.
- Universal 1/r^3 quantitative law: not found as such in the four supplied HTMLs; audit the later task specification separately.
- NumPy2.5.5 already executed and pixel-exact output guaranteed: revised HTMLs explicitly preserve test/rendering limits.

## Limitations

- No full link-health crawl: canonical ShmooCon defect, source citations already researched and placeholders were checked.
- No verification of editorial review, external DOI deposits or undisclosed original captures was possible.
- The URH-NG AI fork and the claimed custom Manchester decoder were not validated.
- Clinical comparator numerical claims were not newly re-audited in this patch pass.
- No hardware action, patient-device interaction, RF capture or original-source mutation occurred.

Delivery rubric: traceability achieved through exact source locators and hashes; precision improved by separating corrections from retained text; reproducibility preserved through explicit historical/new-result separation; completeness bounded to the four HTMLs and cited audits. Publication status, clinical conclusions and unseen raw captures remain unverified.


---

## Appendix G Presenter and catalog coverage

# Coverage extension — presenter leads and conference catalogs

Version 1.0 • accessed 2026-11-20 • bounded source-index screen.

This extension screened **149 presentation appearances on 12 profiles for 11 requested people**, yielding **141 distinct title/event-date leads** after shared-presenter duplicates. It opened **42 additional talk pages**: **29 relevant abstract-level additions, 6 peripheral exclusions, and 7 unresolved pages without descriptions**. Across the unique profile leads, 38 were already represented in Workstreams A–C, 29 were additional relevant items, 67 were peripheral exclusions, and 7 remain unresolved. None of these counts means 141 recordings watched.

InfoconDB is the primary source for its catalog contents and an aggregator for underlying research. “Reviewed” here means the indexed metadata and abstract were read; it does not imply that advertised demonstrations occurred, that a recording was watched, or that technical results were reproduced. Historical dates and listed durations are schedule metadata. Workstream A separately documents Dodge recording/transcript review and its limits.

## Screening rules and validation

- Included explicit RF/SDR/PHY/protocol/receiver methods, medical-device cybersecurity, and selected healthcare governance context. Consumer radios, optical analogies and governance panels are labeled separately from CI-specific evidence.
- Matched prior records by normalized title and exact indexed event date. Repeat editions remain separate; shared-presenter occurrences collapse only for unique counts. Josh/Joshua Corman aliases were both checked.
- Excluded unrelated titles conservatively and recorded title-only review depth. All missing-description leads remain unresolved; a relevant speaker biography is not evidence of session contents.
- Validation: 149 rows have a disposition; counts sum to 149; unique-title/date counts sum to 141; 42 added pages have exact URLs and web references; all 11 series have catalog records. The accompanying JSON preserves every occurrence and edition counter.

## Presenter coverage

| Profile | Listed appearances | Already represented | Additional relevant | Peripheral excluded | Unresolved | Source ref |
|---|---:|---:|---:|---:|---:|---|
| [Barnaby Jack](https://infocondb.org/presenter/barnaby-jack) | 3 | 1 | 0 | 2 | 0 | `turn843884247view1` |
| [Jay Radcliffe](https://infocondb.org/presenter/jay-radcliffe) | 10 | 4 | 3 | 3 | 0 | `turn843884247view2` |
| [Billy Rios](https://infocondb.org/presenter/billy-rios) | 8 | 4 | 0 | 4 | 0 | `turn843884247view3` |
| [Joshua Corman](https://infocondb.org/presenter/joshua-corman) | 44 | 6 | 4 | 34 | 0 | `turn843884247view4` |
| [Michael Ossmann](https://infocondb.org/presenter/michael-ossmann) | 27 | 8 | 8 | 6 | 5 | `turn453789724view0` |
| [Matt Knight](https://infocondb.org/presenter/matt-knight) | 7 | 5 | 2 | 0 | 0 | `turn453789724view1` |
| [Marc Newlin](https://infocondb.org/presenter/marc-newlin) | 12 | 4 | 4 | 3 | 1 | `turn453789724view2` |
| [Balint Seeber](https://infocondb.org/presenter/balint-seeber) | 6 | 6 | 0 | 0 | 0 | `turn453789724view3` |
| [Travis Goodspeed](https://infocondb.org/presenter/travis-goodspeed) | 26 | 4 | 8 | 12 | 2 | `turn453789724view4` |
| [Josh Corman](https://infocondb.org/presenter/josh-corman) | 4 | 0 | 0 | 4 | 0 | `turn395130611view2` |
| [Kevin Fu](https://infocondb.org/presenter/kevin-fu) | 1 | 1 | 0 | 0 | 0 | `turn378295121view6` |
| [Jeff Dodge](https://infocondb.org/presenter/jeff-dodge) | 1 | 1 | 0 | 0 | 0 | `turn759378408view1` |

Counts describe these profiles, not each person's full career. Kevin Fu and Jeff Dodge each have one listed presentation in the retrieved profile. Josh/Joshua Corman split across two pages demonstrates alias-related recall risk. The supplied profile of Jay Radcliffe does not list every historical talk already found in Workstream B.

## Conference-series catalog coverage

These are **catalog counters, not titles screened in this extension**. A zero denotes an empty indexed edition, not proof that the event had no presentations. The JSON lists every edition and any cancellation/virtual/rescheduling flag. Series totals can include workshops, panels and other presentation types; they are not media-file counts.

| Series | Indexed date range | Editions | Nonempty | Empty | Presentation counter sum | Source ref |
|---|---|---:|---:|---:|---:|---|
| [DEF CON](https://infocondb.org/con/def-con/) | 1993-06-09 to 2025-08-07 | 36 | 31 | 5 | 3140 | `turn378295121view0` |
| [Black Hat](https://infocondb.org/con/black-hat/) | 1997-07-09 to 2025-08-02 | 75 | 32 | 43 | 2160 | `turn378295121view1` |
| [ShmooCon](https://infocondb.org/con/shmoocon/) | 2005-02-04 to 2025-01-10 | 20 | 10 | 10 | 413 | `turn378295121view2` |
| [REcon](https://infocondb.org/con/recon/) | 2005-06-17 to 2025-06-27 | 19 | 17 | 2 | 397 | `turn378295121view3` |
| [CCC](https://infocondb.org/con/ccc/) | 1999-12-27 to 2024-12-27 | 25 | 4 | 21 | 638 | `turn378295121view4` |
| [TROOPERS](https://infocondb.org/con/troopers/) | 2008-04-22 to 2018-03-12 | 11 | 3 | 8 | 171 | `turn378295121view5` |
| [ToorCon](https://infocondb.org/con/toorcon/) | 1999-09-03 to 2024-06-26 | 34 | 20 | 14 | 726 | `turn657538463view0` |
| [DerbyCon](https://infocondb.org/con/derbycon/) | 2011-09-30 to 2019-09-04 | 9 | 7 | 2 | 792 | `turn657538463view1` |
| [Kernelcon](https://infocondb.org/con/kernelcon/) | 2019-04-05 to 2025-04-03 | 7 | 4 | 3 | 145 | `turn657538463view2` |
| [BSides Las Vegas](https://infocondb.org/con/security-bsides/) | 2009-07-29 to 2023-08-08 | 15 | 6 | 9 | 761 | `turn657538463view3` |
| [HOPE](https://infocondb.org/con/hope/) | 1994-08-13 to 2025-08-15 | 16 | 14 | 2 | 1301 | `turn657538463view4` |

Material catalog gaps:

- Black Hat: all listed 2023–2025 editions have zero indexed presentations; USA 2022 is the latest populated edition in this snapshot. The range is not continuous populated coverage.
- CCC: only 30C3–33C3 have nonzero counters. TROOPERS ends at 2018, with only 2016–2018 populated. These catalogs cannot support modern or all-year completeness claims.
- ShmooCon, REcon, Kernelcon and HOPE have empty 2024/2025 editions. ShmooCon also has earlier gaps, including 2020; the 44-session ShmooCon XIII screen is a separate complete screen of that retrieved edition only.
- BSides Las Vegas: 15 LV editions were selected from 44 regional entries; six are populated. 2018 and 2020–2022 are empty in this index. Regional BSides totals were not substituted for LV coverage.
- ToorCon includes San Diego, Seattle and ToorCamp branches; DerbyCon has empty 2014/2015 editions. Kernelcon's four nonempty editions total 145 entries, but their individual session titles were not screened in this extension.

## Additional talk-page review

All rows below were opened. “Additional relevant reviewed” retains methodological or contextual relevance; it does not make the talk direct CI/NFMI evidence. The 7 unresolved rows need source descriptions or actual media inspection before substantive use. No new full media review was performed.

| ID | Session / date / conference | Presenters | Disposition / relevance | Reason and limits | Web ref |
|---|---|---|---|---|---|
| E01 | [State Of Healthcare Cyber Safety](https://infocondb.org/con/security-bsides/bsideslv-2016/state-of-healthcare-cyber-safety)<br>2016-08-02; BSidesLV 2016 | Colin Morgan; Jay Radcliffe; Beau Woods; Suzanne Schwartz, MD; Christian Dameff MD MS / quaddi  as Christian Dameff | additional relevant reviewed; medical-context | Historical medical-device coordination and safety panel; useful governance context, not CI/NFMI signal evidence. | `turn185966875view0` |
| E02 | [Medical Devices Roundtable: Is There a Doctor in the House? Security and Privacy in the Medical World](https://infocondb.org/con/black-hat/black-hat-usa-2014/medical-devices-roundtable-is-there-a-doctor-in-the-house-security-and-privacy-in-the-medical-world)<br>2014-08-07; Black Hat USA 2014 | Jay Radcliffe | additional relevant reviewed; medical-context | Connected-medical-device security/privacy roundtable; contextual, with no CI-specific physical-layer measurement claim. | `turn185966875view1` |
| E03 | [Fact and Fiction: Defending your Medical Devices](https://infocondb.org/con/black-hat/black-hat-usa-2013/fact-and-fiction-defending-your-medical-devices)<br>2013-07-31; Black Hat USA 2013 | Jay Radcliffe | additional relevant reviewed; medical-methodology | Historical device-maintenance and coordinated-disclosure framework; abstract promises a software-bug demonstration, not proof of an RF result. | `turn185966875view2` |
| E04 | [IATC Cyber Crisis Simulation](https://infocondb.org/con/security-bsides/bsideslv-2017/iatc-cyber-crisis-simulation)<br>2017-07-26; BSidesLV 2017 | Beau Woods; Jay Healey; Joshua Corman | peripheral excluded; peripheral | Abstract describes general nationwide cyber-crisis policy simulation; no specific medical-device/RF characterization method. | `turn185966875view3` |
| E05 | [HHS Task Force (Panel)](https://infocondb.org/con/security-bsides/bsideslv-2017/hhs-task-force-panel)<br>2017-07-25; BSidesLV 2017 | Joshua Corman | additional relevant reviewed; medical-context | Historical HHS task-force process and recommendations panel; healthcare governance context only. | `turn185966875view4` |
| E06 | [Healthcare in Critical Condition](https://infocondb.org/con/security-bsides/bsideslv-2017/healthcare-in-critical-condition)<br>2017-07-25; BSidesLV 2017 | Jeff Tully MD / r3plicant   as Jeff Tulley; Joshua Corman; Christian Dameff MD MS / quaddi   as Christian Dameff | additional relevant reviewed; medical-context | Historical healthcare incidents, manufacturer/researcher collaboration and policy discussion; not a CI vulnerability finding. | `turn185966875view5` |
| E07 | [Keynote](https://infocondb.org/con/troopers/troopers18/keynote)<br>2018-03-14; TROOPERS18 (2018) | Michael Ossmann   as Mike Ossmann | unresolved; unresolved | Generic keynote title and no indexed abstract; relevance cannot be determined from this page. | `turn185966875view6` |
| E08 | [Pseudo-Doppler Redux](https://infocondb.org/con/shmoocon/shmoocon-xiv/pseudo-doppler-redux)<br>2018-01-19; ShmooCon XIV (2018) | Michael Ossmann; Schuyler St. Leger | unresolved; unresolved | RF-suggestive title but no indexed abstract; no verified direction-finding content or transferability. | `turn185966875view7` |
| E09 | [Exploring The Infrared World, Part 2](https://infocondb.org/con/troopers/troopers17/exploring-the-infrared-world-part-2)<br>2017-03-23; TROOPERS17 (2017) | Dominic Spill; Michael Ossmann   as Mike Ossmann | additional relevant reviewed; methodological | DSP techniques adapted from RF to infrared. Optical analogue for unknown-signal reasoning; does not establish RF or CI behavior. | `turn185966875view8` |
| E10 | [The NSA Playset: RF Retroreflectors](https://infocondb.org/con/def-con/def-con-22/the-nsa-playset-rf-retroreflectors)<br>2014-08-08; DEF CON 22 (2014) | Michael Ossmann | additional relevant reviewed; RF-context | Historical backscatter/retroreflector presentation. Distinct physical mechanism from an implanted CI inductive link; no construction procedure reproduced. | `turn185966875view9` |
| E11 | [HackRF: A Low Cost Software Defined Radio Platform](https://infocondb.org/con/toorcon/toorcon-san-diego-14/hackrf-a-low-cost-software-defined-radio-platform)<br>2012-10-20; ToorCon San Diego 14 (2012) | Michael Ossmann; Jared Boone | additional relevant reviewed; RF-methodology | Historical HackRF platform introduction; establishes an SDR research-tool lineage, not present specifications or suitability. | `turn185966875view10` |
| E12 | [Spread Spectrum Clock Generation, Emission Security, and You](https://infocondb.org/con/toorcon/toorcon-seattle-2011/spread-spectrum-clock-generation-emission-security-and-you)<br>2011-06-18; ToorCon: Seattle 2011 | Michael Ossmann | unresolved; unresolved | Relevant emissions/spread-spectrum title with no indexed abstract; no technical conclusions extracted. | `turn185966875view11` |
| E13 | [Hacking the CampCopter](https://infocondb.org/con/toorcon/toorcamp-2016/hacking-the-campcopter)<br>2016-06-09; ToorCamp 2016 | Michael Ossmann; Dominic Spill | additional relevant reviewed; RF-methodology | Toy-quadcopter radio/firmware case study; illustrates separate radio and embedded interfaces, without any medical transfer claim. | `turn506378219view0` |
| E14 | [Ubertooth Zero, a preview](https://infocondb.org/con/toorcon/toorcon-san-diego-12/ubertooth-zero-a-preview)<br>2010-10-24; ToorCon San Diego 12 (2010) | Michael Ossmann | unresolved; unresolved | Named radio-tool preview but no indexed abstract; details and media content not verified. | `turn506378219view1` |
| E15 | [Real Men Carry Pink Pagers](https://infocondb.org/con/toorcon/toorcon-san-diego-12/real-men-carry-pink-pagers)<br>2010-10-23; ToorCon San Diego 12 (2010) | Travis Goodspeed; Michael Ossmann | unresolved; unresolved | No indexed abstract; pager-related title and co-presenters alone do not verify technique. | `turn506378219view2` |
| E16 | [Bluetooth, Smells Like Chicken](https://infocondb.org/con/def-con/def-con-17/bluetooth-smells-like-chicken)<br>2009-08-01; DEF CON 17 (2009) | Mark Steward; Dominic Spill; Michael Ossmann | additional relevant reviewed; RF-methodology | Historical passive Bluetooth-monitoring and hopping-analysis work; illustrates channel/hopping constraints, not NFMI equivalence. | `turn506378219view3` |
| E17 | [Designing and Applying Extensible RF Fuzzing Tools to Expose PHY Layer Vulnerabilities](https://infocondb.org/con/def-con/def-con-26/designing-and-applying-extensible-rf-fuzzing-tools-to-expose-phy-layer-vulnerabilities)<br>2018-08-12; DEF CON 26 (2018) | Matt Knight; Ryan Speers | additional relevant reviewed; RF-context | PHY fuzzing tools TumbleRF/Orthrus described in abstract; retain as test-framework context only, with no active procedure. | `turn506378219view4` |
| E18 | [Unifying RF Fuzzing Techniques under a Common API: Introducing unfAPI](https://infocondb.org/con/troopers/troopers18/unifying-rf-fuzzing-techniques-under-a-common-api-introducing-unfapi)<br>2018-03-15; TROOPERS18 (2018) | Matt Knight; Ryan Speers | additional relevant reviewed; RF-context | Wireless-fuzzing API/framework history; relevant tool architecture, outside passive-only experimental work. | `turn506378219view5` |
| E19 | [TBA](https://infocondb.org/con/toorcon/toorcon-san-diego-19/tba)<br>2017-09-02; ToorCon San Diego 19 (2017) | Marc Newlin; Logan Lamb; Chris Grayson | unresolved; unresolved | TBA and no abstract. Presenter biographies are insufficient evidence to infer this session's subject. | `turn506378219view6` |
| E20 | [CableTap: Wirelessly Tapping Your Home Network](https://infocondb.org/con/def-con/def-con-25/cabletap-wirelessly-tapping-your-home-network)<br>2017-07-29; DEF CON 25 (2017) | Marc Newlin; Logan Lamb; Chris Grayson | additional relevant reviewed; RF-context | Consumer gateway/set-top-box vulnerability case study; wireless-system context, not near-field measurement methodology. | `turn506378219view7` |
| E21 | [Pwn all the Peripherals: MouseJack, KeyJack, and KeySniffer](https://infocondb.org/con/toorcon/toorcon-san-diego-18/pwn-all-the-peripherals-mousejack-keyjack-and-keysniffer)<br>2016-10-15; ToorCon San Diego 18 (2016) | Marc Newlin | additional relevant reviewed; RF-methodology | Wireless peripheral research with security-implementation implications; consumer hardware case study, not medical evidence. | `turn506378219view8` |
| E22 | [MouseJack: Injecting Keystrokes into Wireless Mice](https://infocondb.org/con/def-con/def-con-24/mousejack-injecting-keystrokes-into-wireless-mice)<br>2016-08-06; DEF CON 24 (2016) | Marc Newlin | additional relevant reviewed; RF-methodology | Non-Bluetooth peripheral protocol/receiver implementation case study; shows why encryption/capability assumptions need device-specific validation. | `turn506378219view9` |
| E23 | [Hacking Wireless Mice with an NES Controller](https://infocondb.org/con/toorcon/toorcon-san-diego-17/hacking-wireless-mice-with-an-nes-controller)<br>2015-10-24; ToorCon San Diego 17 (2015) | Marc Newlin | additional relevant reviewed; RF-methodology | Earlier Logitech peripheral reverse-engineering case study; separates passive observations from described active demonstrations. | `turn506378219view10` |
| E24 | [Building a Damned Good Watch: Counterfeiting a Calculator Watch with a Radio and Disassembler](https://infocondb.org/con/recon/recon-2018/building-a-damned-good-watch-counterfeiting-a-calculator-watch-with-a-radio-and-disassembler)<br>2018-06-15; REcon 2018 | Travis Goodspeed | additional relevant reviewed; RF-methodology | Sub-GHz radio hardware in a replacement calculator watch; contextual receiver/hardware case study, no CI equivalence. | `turn965733281view0` |
| E25 | [Building a GoodWatch](https://infocondb.org/con/shmoocon/shmoocon-xiv/building-a-goodwatch)<br>2018-01-20; ShmooCon XIV (2018) | Travis Goodspeed | unresolved; unresolved | No indexed abstract. A later GoodWatch-related talk exists, but identical content is not assumed. | `turn965733281view1` |
| E26 | [Hillbilly Tracking of Low Earth Orbit: Repurposing an Inmarsat Dish](https://infocondb.org/con/ccc/30c3/hillbilly-tracking-of-low-earth-orbit-repurposing-an-inmarsat-dish)<br>2013-12-28; 30C3 (2013) | Travis Goodspeed | additional relevant reviewed; RF-methodology | Satellite tracking and spectral/SDR recording architecture; methodological logging context with very different propagation geometry. | `turn965733281view2` |
| E27 | [Portscanning Low Earth Orbit](https://infocondb.org/con/summercon/summercon-2013/portscanning-low-earth-orbit)<br>2013-06-07; Summercon 2013 | Travis Goodspeed | additional relevant reviewed; RF-methodology | Related maritime-dish/satellite-tracking architecture; separate event, no assumption of identical recording or content. | `turn965733281view3` |
| E28 | [Exploiting ZigBee and the Internet of Things](https://infocondb.org/con/hope/hope-number-nine/exploiting-zigbee-and-the-internet-of-things)<br>2012-07-13; HOPE Number Nine (2012) | Travis Goodspeed | additional relevant reviewed; RF-context | ZigBee hardware and cryptographic case studies; supports layer-boundary awareness, not inference that another protocol has these weaknesses. | `turn965733281view4` |
| E29 | [Remotely Exploiting the Digital Radio PHY Layer Without Owning a Radio](https://infocondb.org/con/toorcon/toorcon-san-diego-13/remotely-exploiting-the-digital-radio-phy-layer-without-owning-a-radio)<br>2011-10-09; ToorCon San Diego 13 (2011) | Travis Goodspeed; Sergey Bratus | additional relevant reviewed; RF-methodology | PHY framing/data-versus-signaling case study; useful parser-boundary concept, no exploit procedure reproduced. | `turn965733281view5` |
| E30 | [Abusing Hardware Defined Radios](https://infocondb.org/con/recon/recon-2011/abusing-hardware-defined-radios)<br>2011-07-08; REcon 2011 | Travis Goodspeed | additional relevant reviewed; RF-methodology | Commodity-radio reception and synchronization constraints for unknown frame markers; methodological context. | `turn965733281view6` |
| E31 | [Building and Breaking the Next HOPE Badge](https://infocondb.org/con/hope/the-next-hope/building-and-breaking-the-next-hope-badge)<br>2010-07-17; The Next HOPE (2010) | Travis Goodspeed | additional relevant reviewed; RF-context | Conference-badge hardware/firmware and radio-repurposing context; active uses mentioned by source are outside this plan. | `turn965733281view7` |
| E32 | [The OpenAMD Project](https://infocondb.org/con/hope/the-next-hope/the-openamd-project)<br>2010-07-16; The Next HOPE (2010) | aestetix  as Aestetix; Travis Goodspeed; Echo; Mitch Altman; Far McKon; cpfr | peripheral excluded; peripheral | Conference-badge social/location platform overview; no substantive RF-characterization or medical-device method in abstract. | `turn965733281view8` |
| E33 | [Locally Exploiting Wireless Sensors](https://infocondb.org/con/def-con/def-con-17/locally-exploiting-wireless-sensors)<br>2009-07-31; DEF CON 17 (2009) | Travis Goodspeed | additional relevant reviewed; RF-context | Local hardware access to wireless-sensor key handling; distinguishes physical-bus observations from over-the-air inference. | `turn965733281view9` |
| E34 | [The NSA Playset: A Year of Toys and Tools](https://infocondb.org/con/black-hat/black-hat-usa-2015/the-nsa-playset-a-year-of-toys-and-tools)<br>2015-08-06; Black Hat USA 2015 | Michael Ossmann | additional relevant reviewed; RF-context | Mixed wired/radio tool survey including Bluetooth and RF retroreflectors; contextual toolkit history only. | `turn617531591view0` |
| E35 | [The NSA Playset](https://infocondb.org/con/toorcon/toorcamp-2014/the-nsa-playset)<br>2014-07-12; ToorCamp 2014 | Michael Ossmann; Dean Pierce / @deanpierce   as Dean Pierce | additional relevant reviewed; RF-context | Mixed radio/wired surveillance-tool history; no implant-medical meaning or CI transfer inferred. | `turn617531591view1` |
| E36 | [Unambiguous Encapsulation - Separating Data and Signaling](https://infocondb.org/con/shmoocon/shmoocon-x/unambiguous-encapsulation-separating-data-and-signaling)<br>2014-01-18; ShmooCon X (2014) | Dominic Spill; Michael Ossmann | additional relevant reviewed; RF-methodology | Error-correcting/encapsulation approach to data-versus-signaling confusion in ZigBee/Ethernet; protocol boundary concept. | `turn617531591view2` |
| E37 | [Where bits & bytes meet flesh & blood: Devops, Cybersafety, and the Internet of Things](https://infocondb.org/con/owasp/appsec-usa-2016/where-bits-bytes-meet-flesh-blood-devops-cybersafety-and-the-internet-of-things)<br>2016-10-14; AppSec USA 2016 | Joshua Corman | peripheral excluded; peripheral | DevOps and general cyber-physical safety strategy; no device-specific RF/medical characterization in abstract. | `turn617531591view3` |
| E38 | [Should there be an Underwriters Laboratories certification for software in IoT products?](https://infocondb.org/con/owasp/appsec-usa-2016/should-there-be-an-underwriters-laboratories-certification-for-software-in-iot-products)<br>2016-10-13; AppSec USA 2016 | Kevin Greene; Anita D'Amico; Joshua Corman | additional relevant reviewed; medical-context | Historical software-assurance/certification debate includes infusion pumps; contextual policy, not current regulatory guidance. | `turn617531591view4` |
| E39 | [The Cavalry Year[0] & a Path Forward for Public Safety](https://infocondb.org/con/def-con/def-con-22/the-cavalry-year0-a-path-forward-for-public-safety)<br>2014-08-09; DEF CON 22 (2014) | Nicholas J. Percoco; Joshua Corman | additional relevant reviewed; medical-context | I Am The Cavalry history explicitly includes medical technology among four sectors; governance context only. | `turn617531591view5` |
| E40 | [The Cavalry Is Us: Protecting the public good](https://infocondb.org/con/owasp/appsec-usa-2013/the-cavalry-is-us-protecting-the-public-good)<br>2013-11-20; AppSec USA 2013 | Joshua Corman; Nicholas J. Percoco | peripheral excluded; peripheral | General advocacy and research-policy organizing; no specific RF or medical technical case in abstract. | `turn617531591view6` |
| E41 | [The Cavalry Is Us: Protecting the public good and our profession](https://infocondb.org/con/derbycon/derbycon-30-all-in-the-family/the-cavalry-is-us-protecting-the-public-good-and-our-profession)<br>2013-09-28; DerbyCon 3.0 All in the Family (2013) | Joshua Corman | peripheral excluded; peripheral | General public-good/research-policy organizing; no specific RF or medical technical case in abstract. | `turn617531591view7` |
| E42 | [The Cavalry Isn't Coming: Starting the Revolution to Fsck it All!](https://infocondb.org/con/def-con/def-con-21/the-cavalry-isnt-coming-starting-the-revolution-to-fsck-it-all)<br>2013-08-04; DEF CON 21 (2013) | Nicholas J. Percoco; Joshua Corman | peripheral excluded; peripheral | General security-community/policy mobilization; no specific RF or medical technical case in abstract. | `turn617531591view8` |

## Complete profile occurrence ledger

This ledger preserves repeated appearances in different profiles. A talk URL is supplied where opened here or already in A–C; otherwise the link points to the inspected profile, which contains the title. “Already reviewed” is a cross-reference to the earlier workstream's stated review depth, including its unresolved details; it does not upgrade the evidence.

| # | Profile presenter | Date / event | Title | Disposition / record | Review basis |
|---:|---|---|---|---|---|
| 1 | [Barnaby Jack](https://infocondb.org/presenter/barnaby-jack) | 2013-08-01; Black Hat USA 2013 | [Implantable Medical Devices: Hacking Humans](https://infocondb.org/con/black-hat/black-hat-usa-2013/implantable-medical-devices-hacking-humans) | already reviewed; B02 | See prior workstream record; `turn843884247view1` |
| 2 | [Barnaby Jack](https://infocondb.org/presenter/barnaby-jack) | 2010-07-31; DEF CON 18 (2010) | [Jackpotting Automated Teller Machines Redux](https://infocondb.org/presenter/barnaby-jack) | peripheral excluded; — | Profile title screen only; `turn843884247view1` |
| 3 | [Barnaby Jack](https://infocondb.org/presenter/barnaby-jack) | 2010-07-28; Black Hat USA 2010 | [Jackpotting Automated Teller Machines Redux](https://infocondb.org/presenter/barnaby-jack) | peripheral excluded; — | Profile title screen only; `turn843884247view1` |
| 4 | [Jay Radcliffe](https://infocondb.org/presenter/jay-radcliffe) | 2019-08-09; DEF CON 27 (2019) | [D0 N0 H4RM: A Healthcare Security Conversation](https://infocondb.org/con/def-con/def-con-27/d0-n0-h4rm-a-healthcare-security-conversation) | already reviewed; B10 | See prior workstream record; `turn843884247view2` |
| 5 | [Jay Radcliffe](https://infocondb.org/presenter/jay-radcliffe) | 2018-08-10; DEF CON 26 (2018) | [D0 N0 H4RM: A Healthcare Security Conversation](https://infocondb.org/con/def-con/def-con-26/d0-n0-h4rm-a-healthcare-security-conversation) | already reviewed; B09 | See prior workstream record; `turn843884247view2` |
| 6 | [Jay Radcliffe](https://infocondb.org/presenter/jay-radcliffe) | 2018-08-08; Black Hat USA 2018 | [Mental Health Hacks: Fighting Burnout, Depression and Suicide in the Hacker Community](https://infocondb.org/presenter/jay-radcliffe) | peripheral excluded; — | Profile title screen only; `turn843884247view2` |
| 7 | [Jay Radcliffe](https://infocondb.org/presenter/jay-radcliffe) | 2017-07-29; DEF CON 25 (2017) | [D0 No H4RM: A Healthcare Security Conversation](https://infocondb.org/con/def-con/def-con-25/d0-no-h4rm-a-healthcare-security-conversation) | already reviewed; B08 | See prior workstream record; `turn843884247view2` |
| 8 | [Jay Radcliffe](https://infocondb.org/presenter/jay-radcliffe) | 2016-09-24; DerbyCon 6.0 Recharge (2016) | [Five year checkup: the state of insulin pump security](https://infocondb.org/con/derbycon/derbycon-60-recharge/five-year-checkup-the-state-of-insulin-pump-security) | already reviewed; B04 | See prior workstream record; `turn843884247view2` |
| 9 | [Jay Radcliffe](https://infocondb.org/presenter/jay-radcliffe) | 2016-08-03; BSidesLV 2016 | [That Which Must Not Be Spoken Of: A Personal Look at Mental Health in Infosec](https://infocondb.org/presenter/jay-radcliffe) | peripheral excluded; — | Profile title screen only; `turn843884247view2` |
| 10 | [Jay Radcliffe](https://infocondb.org/presenter/jay-radcliffe) | 2016-08-02; BSidesLV 2016 | [State Of Healthcare Cyber Safety](https://infocondb.org/con/security-bsides/bsideslv-2016/state-of-healthcare-cyber-safety) | additional relevant reviewed; E01 | Indexed talk page and abstract (if available); `turn185966875view0` |
| 11 | [Jay Radcliffe](https://infocondb.org/presenter/jay-radcliffe) | 2014-08-07; Black Hat USA 2014 | [Medical Devices Roundtable: Is There a Doctor in the House? Security and Privacy in the Medical World](https://infocondb.org/con/black-hat/black-hat-usa-2014/medical-devices-roundtable-is-there-a-doctor-in-the-house-security-and-privacy-in-the-medical-world) | additional relevant reviewed; E02 | Indexed talk page and abstract (if available); `turn185966875view1` |
| 12 | [Jay Radcliffe](https://infocondb.org/presenter/jay-radcliffe) | 2014-08-06; BSidesLV 2014 | [Booze, Devil's Advocate, and Hugs: the Best Debates Panel You'll See at BSidesLV 2014](https://infocondb.org/presenter/jay-radcliffe) | peripheral excluded; — | Profile title screen only; `turn843884247view2` |
| 13 | [Jay Radcliffe](https://infocondb.org/presenter/jay-radcliffe) | 2013-07-31; Black Hat USA 2013 | [Fact and Fiction: Defending your Medical Devices](https://infocondb.org/con/black-hat/black-hat-usa-2013/fact-and-fiction-defending-your-medical-devices) | additional relevant reviewed; E03 | Indexed talk page and abstract (if available); `turn185966875view2` |
| 14 | [Billy Rios](https://infocondb.org/presenter/billy-rios) | 2019-08-09; DEF CON 27 (2019) | [D0 N0 H4RM: A Healthcare Security Conversation](https://infocondb.org/con/def-con/def-con-27/d0-n0-h4rm-a-healthcare-security-conversation) | already reviewed; B10 | See prior workstream record; `turn843884247view3` |
| 15 | [Billy Rios](https://infocondb.org/presenter/billy-rios) | 2018-08-09; Black Hat USA 2018 | [Understanding and Exploiting Implanted Medical Devices](https://infocondb.org/con/black-hat/black-hat-usa-2018/understanding-and-exploiting-implanted-medical-devices) | already reviewed; B05 | See prior workstream record; `turn843884247view3` |
| 16 | [Billy Rios](https://infocondb.org/presenter/billy-rios) | 2017-07-26; Black Hat USA 2017 | [When IoT Attacks: Understanding the Safety Risks Associated with Connected Devices](https://infocondb.org/con/black-hat/black-hat-usa-2017/when-iot-attacks-understanding-the-safety-risks-associated-with-connected-devices) | already reviewed; B07 | See prior workstream record; `turn843884247view3` |
| 17 | [Billy Rios](https://infocondb.org/presenter/billy-rios) | 2015-07-18; Summercon 2015 | [An Examination of Infusion Pump Technology](https://infocondb.org/con/summercon/summercon-2015/an-examination-of-infusion-pump-technology) | already reviewed; B06 | See prior workstream record; `turn843884247view3` |
| 18 | [Billy Rios](https://infocondb.org/presenter/billy-rios) | 2014-08-06; Black Hat USA 2014 | [Pulling Back the Curtain on Airport Security: Can a Weapon Get Past TSA?](https://infocondb.org/presenter/billy-rios) | peripheral excluded; — | Profile title screen only; `turn843884247view3` |
| 19 | [Billy Rios](https://infocondb.org/presenter/billy-rios) | 2014-02-24; BSidesSF 2014 | [ICS and Embedded Security Research – A Primer](https://infocondb.org/presenter/billy-rios) | peripheral excluded; — | Profile title screen only; `turn843884247view3` |
| 20 | [Billy Rios](https://infocondb.org/presenter/billy-rios) | 2011-10-01; DerbyCon 1.0 (2011) | [100 bugs in 100 days: An analysis of ICS (SCADA) software](https://infocondb.org/presenter/billy-rios) | peripheral excluded; — | Profile title screen only; `turn843884247view3` |
| 21 | [Billy Rios](https://infocondb.org/presenter/billy-rios) | 2007-08-05; DEF CON 15 (2007) | [Biting tha Hand that Feeds You - Storing and Serving Malicous Content >From Well Known Web Servers](https://infocondb.org/presenter/billy-rios) | peripheral excluded; — | Profile title screen only; `turn843884247view3` |
| 22 | [Joshua Corman](https://infocondb.org/presenter/joshua-corman) | 2022-08-13; DEF CON 30 (2022) | [D0 N0 H4RM: A Healthcare Security Conversation (Lounge)](https://infocondb.org/con/def-con/def-con-30/d0-n0-h4rm-a-healthcare-security-conversation-lounge) | already reviewed; B13 | See prior workstream record; `turn843884247view4` |
| 23 | [Joshua Corman](https://infocondb.org/presenter/joshua-corman) | 2021-08-06; DEF CON 29 (2021) | [D0 N0 H4RM: A Healthcare Security Conversation](https://infocondb.org/con/def-con/def-con-29/d0-n0-h4rm-a-healthcare-security-conversation) | already reviewed; B12 | See prior workstream record; `turn843884247view4` |
| 24 | [Joshua Corman](https://infocondb.org/presenter/joshua-corman) | 2019-08-06; BSidesLV 2019 | [I Am The Cavalry Track Welcome and Overview](https://infocondb.org/con/security-bsides/bsideslv-2019/i-am-the-cavalry-track-welcome-and-overview) | already reviewed; B15 | See prior workstream record; `turn843884247view4` |
| 25 | [Joshua Corman](https://infocondb.org/presenter/joshua-corman) | 2019-05-03; THOTCON 0xA (2019) | [Where Do We Go From Here?](https://infocondb.org/presenter/joshua-corman) | peripheral excluded; — | Profile title screen only; `turn843884247view4` |
| 26 | [Joshua Corman](https://infocondb.org/presenter/joshua-corman) | 2018-08-10; DEF CON 26 (2018) | [D0 N0 H4RM: A Healthcare Security Conversation](https://infocondb.org/con/def-con/def-con-26/d0-n0-h4rm-a-healthcare-security-conversation) | already reviewed; B09 | See prior workstream record; `turn843884247view4` |
| 27 | [Joshua Corman](https://infocondb.org/presenter/joshua-corman) | 2017-09-23; DerbyCon 7.0 Legacy (2017) | [Anatomy of a Medical Device Hack- Doctors vs. Hackers in a Clinical Simulation Cage Match](https://infocondb.org/con/derbycon/derbycon-70-legacy/anatomy-of-a-medical-device-hack-doctors-vs-hackers-in-a-clinical-simulation-cage-match) | already reviewed; B14 | See prior workstream record; `turn843884247view4` |
| 28 | [Joshua Corman](https://infocondb.org/presenter/joshua-corman) | 2017-07-30; DEF CON 25 (2017) | [DC to DEF CON: Q&A with Congressmen James Langevin and Will Hurd](https://infocondb.org/presenter/joshua-corman) | peripheral excluded; — | Profile title screen only; `turn843884247view4` |
| 29 | [Joshua Corman](https://infocondb.org/presenter/joshua-corman) | 2017-07-29; DEF CON 25 (2017) | [D0 No H4RM: A Healthcare Security Conversation](https://infocondb.org/con/def-con/def-con-25/d0-no-h4rm-a-healthcare-security-conversation) | already reviewed; B08 | See prior workstream record; `turn843884247view4` |
| 30 | [Joshua Corman](https://infocondb.org/presenter/joshua-corman) | 2017-07-26; BSidesLV 2017 | [IATC Cyber Crisis Simulation](https://infocondb.org/con/security-bsides/bsideslv-2017/iatc-cyber-crisis-simulation) | peripheral excluded; E04 | Indexed talk page and abstract (if available); `turn185966875view3` |
| 31 | [Joshua Corman](https://infocondb.org/presenter/joshua-corman) | 2017-07-25; BSidesLV 2017 | [HHS Task Force (Panel)](https://infocondb.org/con/security-bsides/bsideslv-2017/hhs-task-force-panel) | additional relevant reviewed; E05 | Indexed talk page and abstract (if available); `turn185966875view4` |
| 32 | [Joshua Corman](https://infocondb.org/presenter/joshua-corman) | 2017-07-25; BSidesLV 2017 | [Healthcare in Critical Condition](https://infocondb.org/con/security-bsides/bsideslv-2017/healthcare-in-critical-condition) | additional relevant reviewed; E06 | Indexed talk page and abstract (if available); `turn185966875view5` |
| 33 | [Joshua Corman](https://infocondb.org/presenter/joshua-corman) | 2017-07-25; BSidesLV 2017 | [IATC Kickoff](https://infocondb.org/presenter/joshua-corman) | peripheral excluded; — | Profile title screen only; `turn843884247view4` |
| 34 | [Joshua Corman](https://infocondb.org/presenter/joshua-corman) | 2017-07-25; BSidesLV 2017 | [How To Lose Friends and Influence People (An Apology)](https://infocondb.org/presenter/joshua-corman) | peripheral excluded; — | Profile title screen only; `turn843884247view4` |
| 35 | [Joshua Corman](https://infocondb.org/presenter/joshua-corman) | 2016-10-14; AppSec USA 2016 | [Where bits & bytes meet flesh & blood: Devops, Cybersafety, and the Internet of Things](https://infocondb.org/con/owasp/appsec-usa-2016/where-bits-bytes-meet-flesh-blood-devops-cybersafety-and-the-internet-of-things) | peripheral excluded; E37 | Indexed talk page and abstract (if available); `turn617531591view3` |
| 36 | [Joshua Corman](https://infocondb.org/presenter/joshua-corman) | 2016-10-13; AppSec USA 2016 | [Should there be an Underwriters Laboratories certification for software in IoT products?](https://infocondb.org/con/owasp/appsec-usa-2016/should-there-be-an-underwriters-laboratories-certification-for-software-in-iot-products) | additional relevant reviewed; E38 | Indexed talk page and abstract (if available); `turn617531591view4` |
| 37 | [Joshua Corman](https://infocondb.org/presenter/joshua-corman) | 2016-08-03; BSidesLV 2016 | [IATC Closing](https://infocondb.org/presenter/joshua-corman) | peripheral excluded; — | Profile title screen only; `turn843884247view4` |
| 38 | [Joshua Corman](https://infocondb.org/presenter/joshua-corman) | 2016-08-03; BSidesLV 2016 | [Uncomfortable Approaches](https://infocondb.org/presenter/joshua-corman) | peripheral excluded; — | Profile title screen only; `turn843884247view4` |
| 39 | [Joshua Corman](https://infocondb.org/presenter/joshua-corman) | 2016-08-03; BSidesLV 2016 | [Uncomfortable Truths](https://infocondb.org/presenter/joshua-corman) | peripheral excluded; — | Profile title screen only; `turn843884247view4` |
| 40 | [Joshua Corman](https://infocondb.org/presenter/joshua-corman) | 2016-08-03; BSidesLV 2016 | [IATC Day 2: Introduction and Overview](https://infocondb.org/presenter/joshua-corman) | peripheral excluded; — | Profile title screen only; `turn843884247view4` |
| 41 | [Joshua Corman](https://infocondb.org/presenter/joshua-corman) | 2016-08-02; BSidesLV 2016 | [State Of Automotive Cyber Safety](https://infocondb.org/presenter/joshua-corman) | peripheral excluded; — | Profile title screen only; `turn843884247view4` |
| 42 | [Joshua Corman](https://infocondb.org/presenter/joshua-corman) | 2016-08-02; BSidesLV 2016 | [IATC Introduction and Overview](https://infocondb.org/presenter/joshua-corman) | peripheral excluded; — | Profile title screen only; `turn843884247view4` |
| 43 | [Joshua Corman](https://infocondb.org/presenter/joshua-corman) | 2015-09-25; AppSec USA 2015 | [Wait, Wait! Don't pwn Me!](https://infocondb.org/presenter/joshua-corman) | peripheral excluded; — | Profile title screen only; `turn843884247view4` |
| 44 | [Joshua Corman](https://infocondb.org/presenter/joshua-corman) | 2015-09-24; AppSec USA 2015 | [Fireside Chat: The End of SW Security as We Know It; Why This Might be a Good Thing.](https://infocondb.org/presenter/joshua-corman) | peripheral excluded; — | Profile title screen only; `turn843884247view4` |
| 45 | [Joshua Corman](https://infocondb.org/presenter/joshua-corman) | 2015-08-04; BSidesLV 2015 | [Stress, Burnout, Rinse, Repeat](https://infocondb.org/presenter/joshua-corman) | peripheral excluded; — | Profile title screen only; `turn843884247view4` |
| 46 | [Joshua Corman](https://infocondb.org/presenter/joshua-corman) | 2015-08-04; BSidesLV 2015 | [How can we ensure safer Automobiles?](https://infocondb.org/presenter/joshua-corman) | peripheral excluded; — | Profile title screen only; `turn843884247view4` |
| 47 | [Joshua Corman](https://infocondb.org/presenter/joshua-corman) | 2015-08-04; BSidesLV 2015 | [State of Automotive Cyber Safety](https://infocondb.org/presenter/joshua-corman) | peripheral excluded; — | Profile title screen only; `turn843884247view4` |
| 48 | [Joshua Corman](https://infocondb.org/presenter/joshua-corman) | 2015-08-04; BSidesLV 2015 | [I Am The Cavalry Track Introduction and Overview](https://infocondb.org/presenter/joshua-corman) | peripheral excluded; — | Profile title screen only; `turn843884247view4` |
| 49 | [Joshua Corman](https://infocondb.org/presenter/joshua-corman) | 2014-09-18; AppSec USA 2014 | [Not Go Quietly: Adaptive Strategies and Unlikely Teammates](https://infocondb.org/presenter/joshua-corman) | peripheral excluded; — | Profile title screen only; `turn843884247view4` |
| 50 | [Joshua Corman](https://infocondb.org/presenter/joshua-corman) | 2014-08-09; DEF CON 22 (2014) | [The Cavalry Year[0] & a Path Forward for Public Safety](https://infocondb.org/con/def-con/def-con-22/the-cavalry-year0-a-path-forward-for-public-safety) | additional relevant reviewed; E39 | Indexed talk page and abstract (if available); `turn617531591view5` |
| 51 | [Joshua Corman](https://infocondb.org/presenter/joshua-corman) | 2014-08-06; BSidesLV 2014 | [Booze, Devil's Advocate, and Hugs: the Best Debates Panel You'll See at BSidesLV 2014](https://infocondb.org/presenter/joshua-corman) | peripheral excluded; — | Profile title screen only; `turn843884247view4` |
| 52 | [Joshua Corman](https://infocondb.org/presenter/joshua-corman) | 2014-02-24; BSidesSF 2014 | [Influencing Policy/Gov/Mainstream Media](https://infocondb.org/presenter/joshua-corman) | peripheral excluded; — | Profile title screen only; `turn843884247view4` |
| 53 | [Joshua Corman](https://infocondb.org/presenter/joshua-corman) | 2014-02-24; BSidesSF 2014 | [Recap Sunday/Re-intro](https://infocondb.org/presenter/joshua-corman) | peripheral excluded; — | Profile title screen only; `turn843884247view4` |
| 54 | [Joshua Corman](https://infocondb.org/presenter/joshua-corman) | 2014-02-23; BSidesSF 2014 | [Why US... Why NOW...](https://infocondb.org/presenter/joshua-corman) | peripheral excluded; — | Profile title screen only; `turn843884247view4` |
| 55 | [Joshua Corman](https://infocondb.org/presenter/joshua-corman) | 2013-11-21; AppSec USA 2013 | [PANEL: Wait Wait... Don't Pwn Me!](https://infocondb.org/presenter/joshua-corman) | peripheral excluded; — | Profile title screen only; `turn843884247view4` |
| 56 | [Joshua Corman](https://infocondb.org/presenter/joshua-corman) | 2013-11-20; AppSec USA 2013 | [The Cavalry Is Us: Protecting the public good](https://infocondb.org/con/owasp/appsec-usa-2013/the-cavalry-is-us-protecting-the-public-good) | peripheral excluded; E40 | Indexed talk page and abstract (if available); `turn617531591view6` |
| 57 | [Joshua Corman](https://infocondb.org/presenter/joshua-corman) | 2013-09-28; DerbyCon 3.0 All in the Family (2013) | [The Cavalry Is Us: Protecting the public good and our profession](https://infocondb.org/con/derbycon/derbycon-30-all-in-the-family/the-cavalry-is-us-protecting-the-public-good-and-our-profession) | peripheral excluded; E41 | Indexed talk page and abstract (if available); `turn617531591view7` |
| 58 | [Joshua Corman](https://infocondb.org/presenter/joshua-corman) | 2013-08-04; DEF CON 21 (2013) | [The Cavalry Isn't Coming: Starting the Revolution to Fsck it All!](https://infocondb.org/con/def-con/def-con-21/the-cavalry-isnt-coming-starting-the-revolution-to-fsck-it-all) | peripheral excluded; E42 | Indexed talk page and abstract (if available); `turn617531591view8` |
| 59 | [Joshua Corman](https://infocondb.org/presenter/joshua-corman) | 2013-04-26; THOTCON 0x4 (2013) | ["Cyberwar!": Not What We Were Expecting](https://infocondb.org/presenter/joshua-corman) | peripheral excluded; — | Profile title screen only; `turn843884247view4` |
| 60 | [Joshua Corman](https://infocondb.org/presenter/joshua-corman) | 2012-10-25; AppSec USA 2012 | [DevOps Distilled: The DevOps Panel at AppSec USA](https://infocondb.org/presenter/joshua-corman) | peripheral excluded; — | Profile title screen only; `turn843884247view4` |
| 61 | [Joshua Corman](https://infocondb.org/presenter/joshua-corman) | 2012-10-25; AppSec USA 2012 | [Doing the unstuck: How Rugged cultures drive Biz & AppSec Value](https://infocondb.org/presenter/joshua-corman) | peripheral excluded; — | Profile title screen only; `turn843884247view4` |
| 62 | [Joshua Corman](https://infocondb.org/presenter/joshua-corman) | 2012-07-28; DEF CON 20 (2012) | [World War 3.0: Chaos, Control & the Battle for the Net](https://infocondb.org/presenter/joshua-corman) | peripheral excluded; — | Profile title screen only; `turn843884247view4` |
| 63 | [Joshua Corman](https://infocondb.org/presenter/joshua-corman) | 2011-08-06; DEF CON 19 (2011) | [PCI 2.0: Still Compromising Controls and Compromising Security](https://infocondb.org/presenter/joshua-corman) | peripheral excluded; — | Profile title screen only; `turn843884247view4` |
| 64 | [Joshua Corman](https://infocondb.org/presenter/joshua-corman) | 2011-08-06; DEF CON 19 (2011) | ["Whoever Fights Monsters..." Aaron Barr, Anonymous, and Ourselves](https://infocondb.org/presenter/joshua-corman) | peripheral excluded; — | Profile title screen only; `turn843884247view4` |
| 65 | [Joshua Corman](https://infocondb.org/presenter/joshua-corman) | 2010-08-01; DEF CON 18 (2010) | [PCI, Compromising Controls and Compromising Security](https://infocondb.org/presenter/joshua-corman) | peripheral excluded; — | Profile title screen only; `turn843884247view4` |
| 66 | [Michael Ossmann](https://infocondb.org/presenter/michael-ossmann) | 2018-08-10; DEF CON 26 (2018) | [Revolting Radios](https://infocondb.org/con/def-con/def-con-26/revolting-radios) | already reviewed; C07 | See prior workstream record; `turn453789724view0` |
| 67 | [Michael Ossmann](https://infocondb.org/presenter/michael-ossmann) | 2018-03-14; TROOPERS18 (2018) | [Keynote](https://infocondb.org/con/troopers/troopers18/keynote) | unresolved; E07 | Indexed talk page and abstract (if available); `turn185966875view6` |
| 68 | [Michael Ossmann](https://infocondb.org/presenter/michael-ossmann) | 2018-01-19; ShmooCon XIV (2018) | [Pseudo-Doppler Redux](https://infocondb.org/con/shmoocon/shmoocon-xiv/pseudo-doppler-redux) | unresolved; E08 | Indexed talk page and abstract (if available); `turn185966875view7` |
| 69 | [Michael Ossmann](https://infocondb.org/presenter/michael-ossmann) | 2017-07-26; Black Hat USA 2017 | [What's on the Wireless? Automating RF Signal Identification](https://infocondb.org/con/black-hat/black-hat-usa-2017/whats-on-the-wireless-automating-rf-signal-identification) | already reviewed; C05 | See prior workstream record; `turn453789724view0` |
| 70 | [Michael Ossmann](https://infocondb.org/presenter/michael-ossmann) | 2017-06-18; REcon 2017 | [Reverse Engineering DSSS](https://infocondb.org/con/recon/recon-2017/reverse-engineering-dsss) | already reviewed; C06 | See prior workstream record; `turn453789724view0` |
| 71 | [Michael Ossmann](https://infocondb.org/presenter/michael-ossmann) | 2017-03-23; TROOPERS17 (2017) | [Exploring The Infrared World, Part 2](https://infocondb.org/con/troopers/troopers17/exploring-the-infrared-world-part-2) | additional relevant reviewed; E09 | Indexed talk page and abstract (if available); `turn185966875view8` |
| 72 | [Michael Ossmann](https://infocondb.org/presenter/michael-ossmann) | 2017-01-14; ShmooCon XIII (2017) | [Exploring The Infrared World](https://infocondb.org/con/shmoocon/shmoocon-xiii/exploring-the-infrared-world) | already reviewed; A18 | See prior workstream record; `turn453789724view0` |
| 73 | [Michael Ossmann](https://infocondb.org/presenter/michael-ossmann) | 2016-10-16; ToorCon San Diego 18 (2016) | [GreatFET Design Review](https://infocondb.org/presenter/michael-ossmann) | peripheral excluded; — | Profile title screen only; `turn453789724view0` |
| 74 | [Michael Ossmann](https://infocondb.org/presenter/michael-ossmann) | 2016-08-03; Black Hat USA 2016 | [GreatFET: Making GoodFET Great Again](https://infocondb.org/presenter/michael-ossmann) | peripheral excluded; — | Profile title screen only; `turn453789724view0` |
| 75 | [Michael Ossmann](https://infocondb.org/presenter/michael-ossmann) | 2016-06-09; ToorCamp 2016 | [Hacking the CampCopter](https://infocondb.org/con/toorcon/toorcamp-2016/hacking-the-campcopter) | additional relevant reviewed; E13 | Indexed talk page and abstract (if available); `turn506378219view0` |
| 76 | [Michael Ossmann](https://infocondb.org/presenter/michael-ossmann) | 2016-03-17; TROOPERS16 (2016) | [Rapid Radio Reversing](https://infocondb.org/con/troopers/troopers16/rapid-radio-reversing) | already reviewed; C04 | See prior workstream record; `turn453789724view0` |
| 77 | [Michael Ossmann](https://infocondb.org/presenter/michael-ossmann) | 2015-10-24; ToorCon San Diego 17 (2015) | [Rapid Radio Reversing](https://infocondb.org/con/toorcon/toorcon-san-diego-17/rapid-radio-reversing) | already reviewed; C03 | See prior workstream record; `turn453789724view0` |
| 78 | [Michael Ossmann](https://infocondb.org/presenter/michael-ossmann) | 2015-08-06; Black Hat USA 2015 | [The NSA Playset: A Year of Toys and Tools](https://infocondb.org/con/black-hat/black-hat-usa-2015/the-nsa-playset-a-year-of-toys-and-tools) | additional relevant reviewed; E34 | Indexed talk page and abstract (if available); `turn617531591view0` |
| 79 | [Michael Ossmann](https://infocondb.org/presenter/michael-ossmann) | 2015-08-05; BSidesLV 2015 | [Better Spectrum Monitoring with Software Defined Radio](https://infocondb.org/con/security-bsides/bsideslv-2015/better-spectrum-monitoring-with-software-defined-radio) | already reviewed; C02 | See prior workstream record; `turn453789724view0` |
| 80 | [Michael Ossmann](https://infocondb.org/presenter/michael-ossmann) | 2015-01-17; ShmooCon XI (2015) | [NSA Playset: USB Tools](https://infocondb.org/presenter/michael-ossmann) | peripheral excluded; — | Profile title screen only; `turn453789724view0` |
| 81 | [Michael Ossmann](https://infocondb.org/presenter/michael-ossmann) | 2014-08-08; DEF CON 22 (2014) | [The NSA Playset: RF Retroreflectors](https://infocondb.org/con/def-con/def-con-22/the-nsa-playset-rf-retroreflectors) | additional relevant reviewed; E10 | Indexed talk page and abstract (if available); `turn185966875view9` |
| 82 | [Michael Ossmann](https://infocondb.org/presenter/michael-ossmann) | 2014-07-12; ToorCamp 2014 | [The NSA Playset](https://infocondb.org/con/toorcon/toorcamp-2014/the-nsa-playset) | additional relevant reviewed; E35 | Indexed talk page and abstract (if available); `turn617531591view1` |
| 83 | [Michael Ossmann](https://infocondb.org/presenter/michael-ossmann) | 2014-06-27; REcon 2014 | [SDR Tricks with HackRF](https://infocondb.org/con/recon/recon-2014/sdr-tricks-with-hackrf) | already reviewed; C01 | See prior workstream record; `turn453789724view0` |
| 84 | [Michael Ossmann](https://infocondb.org/presenter/michael-ossmann) | 2014-01-18; ShmooCon X (2014) | [Unambiguous Encapsulation - Separating Data and Signaling](https://infocondb.org/con/shmoocon/shmoocon-x/unambiguous-encapsulation-separating-data-and-signaling) | additional relevant reviewed; E36 | Indexed talk page and abstract (if available); `turn617531591view2` |
| 85 | [Michael Ossmann](https://infocondb.org/presenter/michael-ossmann) | 2013-10-19; ToorCon San Diego 15 (2013) | [Multiplexed Wired Attack Surfaces](https://infocondb.org/presenter/michael-ossmann) | peripheral excluded; — | Profile title screen only; `turn453789724view0` |
| 86 | [Michael Ossmann](https://infocondb.org/presenter/michael-ossmann) | 2013-08-01; Black Hat USA 2013 | [Multiplexed Wired Attack Surfaces](https://infocondb.org/presenter/michael-ossmann) | peripheral excluded; — | Profile title screen only; `turn453789724view0` |
| 87 | [Michael Ossmann](https://infocondb.org/presenter/michael-ossmann) | 2013-08-01; Black Hat USA 2013 | [What's on the Wire? Physical Layer Tapping with Project Daisho](https://infocondb.org/presenter/michael-ossmann) | peripheral excluded; — | Profile title screen only; `turn453789724view0` |
| 88 | [Michael Ossmann](https://infocondb.org/presenter/michael-ossmann) | 2012-10-20; ToorCon San Diego 14 (2012) | [HackRF: A Low Cost Software Defined Radio Platform](https://infocondb.org/con/toorcon/toorcon-san-diego-14/hackrf-a-low-cost-software-defined-radio-platform) | additional relevant reviewed; E11 | Indexed talk page and abstract (if available); `turn185966875view10` |
| 89 | [Michael Ossmann](https://infocondb.org/presenter/michael-ossmann) | 2011-06-18; ToorCon: Seattle 2011 | [Spread Spectrum Clock Generation, Emission Security, and You](https://infocondb.org/con/toorcon/toorcon-seattle-2011/spread-spectrum-clock-generation-emission-security-and-you) | unresolved; E12 | Indexed talk page and abstract (if available); `turn185966875view11` |
| 90 | [Michael Ossmann](https://infocondb.org/presenter/michael-ossmann) | 2010-10-24; ToorCon San Diego 12 (2010) | [Ubertooth Zero, a preview](https://infocondb.org/con/toorcon/toorcon-san-diego-12/ubertooth-zero-a-preview) | unresolved; E14 | Indexed talk page and abstract (if available); `turn506378219view1` |
| 91 | [Michael Ossmann](https://infocondb.org/presenter/michael-ossmann) | 2010-10-23; ToorCon San Diego 12 (2010) | [Real Men Carry Pink Pagers](https://infocondb.org/con/toorcon/toorcon-san-diego-12/real-men-carry-pink-pagers) | unresolved; E15 | Indexed talk page and abstract (if available); `turn506378219view2` |
| 92 | [Michael Ossmann](https://infocondb.org/presenter/michael-ossmann) | 2009-08-01; DEF CON 17 (2009) | [Bluetooth, Smells Like Chicken](https://infocondb.org/con/def-con/def-con-17/bluetooth-smells-like-chicken) | additional relevant reviewed; E16 | Indexed talk page and abstract (if available); `turn506378219view3` |
| 93 | [Matt Knight](https://infocondb.org/presenter/matt-knight) | 2018-08-12; DEF CON 26 (2018) | [Designing and Applying Extensible RF Fuzzing Tools to Expose PHY Layer Vulnerabilities](https://infocondb.org/con/def-con/def-con-26/designing-and-applying-extensible-rf-fuzzing-tools-to-expose-phy-layer-vulnerabilities) | additional relevant reviewed; E17 | Indexed talk page and abstract (if available); `turn506378219view4` |
| 94 | [Matt Knight](https://infocondb.org/presenter/matt-knight) | 2018-03-15; TROOPERS18 (2018) | [Unifying RF Fuzzing Techniques under a Common API: Introducing unfAPI](https://infocondb.org/con/troopers/troopers18/unifying-rf-fuzzing-techniques-under-a-common-api-introducing-unfapi) | additional relevant reviewed; E18 | Indexed talk page and abstract (if available); `turn506378219view5` |
| 95 | [Matt Knight](https://infocondb.org/presenter/matt-knight) | 2017-07-28; DEF CON 25 (2017) | [Radio Exploitation 101: Characterizing, Contextualizing, and Applying Wireless Attack Methods](https://infocondb.org/con/def-con/def-con-25/radio-exploitation-101-characterizing-contextualizing-and-applying-wireless-attack-methods) | already reviewed; C11 | See prior workstream record; `turn453789724view1` |
| 96 | [Matt Knight](https://infocondb.org/presenter/matt-knight) | 2017-03-20; TROOPERS17 (2017) | [So You Want to Hack Radios](https://infocondb.org/con/troopers/troopers17/so-you-want-to-hack-radios) | already reviewed; C09 | See prior workstream record; `turn453789724view1` |
| 97 | [Matt Knight](https://infocondb.org/presenter/matt-knight) | 2017-01-14; ShmooCon XIII (2017) | [So You Want to Hack Radios](https://infocondb.org/con/shmoocon/shmoocon-xiii/so-you-want-to-hack-radios) | already reviewed; C08, A16 | See prior workstream record; `turn453789724view1` |
| 98 | [Matt Knight](https://infocondb.org/presenter/matt-knight) | 2016-12-29; 33C3 (2016) | [Decoding the LoRa PHY: Dissecting a Modern Wireless Network for the Internet of Things](https://infocondb.org/con/ccc/33c3/decoding-the-lora-phy-dissecting-a-modern-wireless-network-for-the-internet-of-things) | already reviewed; C13 | See prior workstream record; `turn453789724view1` |
| 99 | [Matt Knight](https://infocondb.org/presenter/matt-knight) | 2016-10-15; ToorCon San Diego 18 (2016) | [Decoding LoRa, A Modern Wireless Network for the Internet of Things](https://infocondb.org/con/toorcon/toorcon-san-diego-18/decoding-lora-a-modern-wireless-network-for-the-internet-of-things) | already reviewed; C14 | See prior workstream record; `turn453789724view1` |
| 100 | [Marc Newlin](https://infocondb.org/presenter/marc-newlin) | 2019-06-01; DEF CON China 1.0 (2019) | [IPv666 - Address of the Beast](https://infocondb.org/presenter/marc-newlin) | peripheral excluded; — | Profile title screen only; `turn453789724view2` |
| 101 | [Marc Newlin](https://infocondb.org/presenter/marc-newlin) | 2019-01-20; ShmooCon XV (2019) | [IPv666: Address of the Beast](https://infocondb.org/presenter/marc-newlin) | peripheral excluded; — | Profile title screen only; `turn453789724view2` |
| 102 | [Marc Newlin](https://infocondb.org/presenter/marc-newlin) | 2018-06-23; ToorCamp 2018 | [The Big, Bad, Cõc Cõc: Tales from a rather suspicious Vietnamese browser](https://infocondb.org/presenter/marc-newlin) | peripheral excluded; — | Profile title screen only; `turn453789724view2` |
| 103 | [Marc Newlin](https://infocondb.org/presenter/marc-newlin) | 2018-03-13; TROOPERS18 (2018) | [Lazy-Mode RF OSINT and Reverse Engineering](https://infocondb.org/con/troopers/troopers18/lazy-mode-rf-osint-and-reverse-engineering) | already reviewed; C12 | See prior workstream record; `turn453789724view2` |
| 104 | [Marc Newlin](https://infocondb.org/presenter/marc-newlin) | 2017-09-02; ToorCon San Diego 19 (2017) | [TBA](https://infocondb.org/con/toorcon/toorcon-san-diego-19/tba) | unresolved; E19 | Indexed talk page and abstract (if available); `turn506378219view6` |
| 105 | [Marc Newlin](https://infocondb.org/presenter/marc-newlin) | 2017-07-29; DEF CON 25 (2017) | [CableTap: Wirelessly Tapping Your Home Network](https://infocondb.org/con/def-con/def-con-25/cabletap-wirelessly-tapping-your-home-network) | additional relevant reviewed; E20 | Indexed talk page and abstract (if available); `turn506378219view7` |
| 106 | [Marc Newlin](https://infocondb.org/presenter/marc-newlin) | 2017-07-28; DEF CON 25 (2017) | [Radio Exploitation 101: Characterizing, Contextualizing, and Applying Wireless Attack Methods](https://infocondb.org/con/def-con/def-con-25/radio-exploitation-101-characterizing-contextualizing-and-applying-wireless-attack-methods) | already reviewed; C11 | See prior workstream record; `turn453789724view2` |
| 107 | [Marc Newlin](https://infocondb.org/presenter/marc-newlin) | 2017-03-20; TROOPERS17 (2017) | [So You Want to Hack Radios](https://infocondb.org/con/troopers/troopers17/so-you-want-to-hack-radios) | already reviewed; C09 | See prior workstream record; `turn453789724view2` |
| 108 | [Marc Newlin](https://infocondb.org/presenter/marc-newlin) | 2017-01-14; ShmooCon XIII (2017) | [So You Want to Hack Radios](https://infocondb.org/con/shmoocon/shmoocon-xiii/so-you-want-to-hack-radios) | already reviewed; C08, A16 | See prior workstream record; `turn453789724view2` |
| 109 | [Marc Newlin](https://infocondb.org/presenter/marc-newlin) | 2016-10-15; ToorCon San Diego 18 (2016) | [Pwn all the Peripherals: MouseJack, KeyJack, and KeySniffer](https://infocondb.org/con/toorcon/toorcon-san-diego-18/pwn-all-the-peripherals-mousejack-keyjack-and-keysniffer) | additional relevant reviewed; E21 | Indexed talk page and abstract (if available); `turn506378219view8` |
| 110 | [Marc Newlin](https://infocondb.org/presenter/marc-newlin) | 2016-08-06; DEF CON 24 (2016) | [MouseJack: Injecting Keystrokes into Wireless Mice](https://infocondb.org/con/def-con/def-con-24/mousejack-injecting-keystrokes-into-wireless-mice) | additional relevant reviewed; E22 | Indexed talk page and abstract (if available); `turn506378219view9` |
| 111 | [Marc Newlin](https://infocondb.org/presenter/marc-newlin) | 2015-10-24; ToorCon San Diego 17 (2015) | [Hacking Wireless Mice with an NES Controller](https://infocondb.org/con/toorcon/toorcon-san-diego-17/hacking-wireless-mice-with-an-nes-controller) | additional relevant reviewed; E23 | Indexed talk page and abstract (if available); `turn506378219view10` |
| 112 | [Balint Seeber](https://infocondb.org/presenter/balint-seeber) | 2018-08-09; Black Hat USA 2018 | [SirenJack: Cracking a 'Secure' Emergency Warning Siren System](https://infocondb.org/con/black-hat/black-hat-usa-2018/sirenjack-cracking-a-secure-emergency-warning-siren-system) | already reviewed; C21 | See prior workstream record; `turn453789724view3` |
| 113 | [Balint Seeber](https://infocondb.org/presenter/balint-seeber) | 2016-01-16; ShmooCon XII (2016) | [Hacking The Wireless World - Software Defined Radio Exploits](https://infocondb.org/con/shmoocon/shmoocon-xii/hacking-the-wireless-world-software-defined-radio-exploits) | already reviewed; C20 | See prior workstream record; `turn453789724view3` |
| 114 | [Balint Seeber](https://infocondb.org/presenter/balint-seeber) | 2015-08-05; BSidesLV 2015 | [All Your RFz Are Belong to Me – Software Defined Radio Exploits](https://infocondb.org/con/security-bsides/bsideslv-2015/all-your-rfz-are-belong-to-me-software-defined-radio-exploits) | already reviewed; C19 | See prior workstream record; `turn453789724view3` |
| 115 | [Balint Seeber](https://infocondb.org/presenter/balint-seeber) | 2014-10-16; Black Hat Europe 2014 | [Hacking the Wireless World with Software Defined Radio - 2.0](https://infocondb.org/con/black-hat/black-hat-europe-2014/hacking-the-wireless-world-with-software-defined-radio-20) | already reviewed; C17 | See prior workstream record; `turn453789724view3` |
| 116 | [Balint Seeber](https://infocondb.org/presenter/balint-seeber) | 2014-08-07; Black Hat USA 2014 | [Hacking the Wireless World with Software Defined Radio - 2.0](https://infocondb.org/con/black-hat/black-hat-usa-2014/hacking-the-wireless-world-with-software-defined-radio-20) | already reviewed; C16 | See prior workstream record; `turn453789724view3` |
| 117 | [Balint Seeber](https://infocondb.org/presenter/balint-seeber) | 2013-08-02; DEF CON 21 (2013) | [All Your RFz Are Belong to Me - Hacking the Wireless World with Software Defined Radio](https://infocondb.org/con/def-con/def-con-21/all-your-rfz-are-belong-to-me-hacking-the-wireless-world-with-software-defined-radio) | already reviewed; C15 | See prior workstream record; `turn453789724view3` |
| 118 | [Travis Goodspeed](https://infocondb.org/presenter/travis-goodspeed) | 2023-06-09; REcon 2023 | [Recent Experiments with Mask ROMs](https://infocondb.org/presenter/travis-goodspeed) | peripheral excluded; — | Profile title screen only; `turn453789724view4` |
| 119 | [Travis Goodspeed](https://infocondb.org/presenter/travis-goodspeed) | 2023-01-21; ShmooCon 2023 | [A Mask ROM Tool in Qt6 and C++](https://infocondb.org/presenter/travis-goodspeed) | peripheral excluded; — | Profile title screen only; `turn453789724view4` |
| 120 | [Travis Goodspeed](https://infocondb.org/presenter/travis-goodspeed) | 2022-03-25; ShmooCon 2022 | [A Web API for Embedded Peripheral Reverse Engineering](https://infocondb.org/presenter/travis-goodspeed) | peripheral excluded; — | Profile title screen only; `turn453789724view4` |
| 121 | [Travis Goodspeed](https://infocondb.org/presenter/travis-goodspeed) | 2018-06-15; REcon 2018 | [Building a Damned Good Watch: Counterfeiting a Calculator Watch with a Radio and Disassembler](https://infocondb.org/con/recon/recon-2018/building-a-damned-good-watch-counterfeiting-a-calculator-watch-with-a-radio-and-disassembler) | additional relevant reviewed; E24 | Indexed talk page and abstract (if available); `turn965733281view0` |
| 122 | [Travis Goodspeed](https://infocondb.org/presenter/travis-goodspeed) | 2018-03-13; TROOPERS18 (2018) | [Frustrating Emulation with Delay Slots in MIPS and MIPS16](https://infocondb.org/presenter/travis-goodspeed) | peripheral excluded; — | Profile title screen only; `turn453789724view4` |
| 123 | [Travis Goodspeed](https://infocondb.org/presenter/travis-goodspeed) | 2018-01-20; ShmooCon XIV (2018) | [Building a GoodWatch](https://infocondb.org/con/shmoocon/shmoocon-xiv/building-a-goodwatch) | unresolved; E25 | Indexed talk page and abstract (if available); `turn965733281view1` |
| 124 | [Travis Goodspeed](https://infocondb.org/presenter/travis-goodspeed) | 2017-01-13; ShmooCon XIII (2017) | [Firetalk #2: Quick and Dirty Emulation of ARM Firmware](https://infocondb.org/con/shmoocon/shmoocon-xiii/firetalk-2-quick-and-dirty-emulation-of-arm-firmware) | already reviewed; A09 | See prior workstream record; `turn453789724view4` |
| 125 | [Travis Goodspeed](https://infocondb.org/presenter/travis-goodspeed) | 2016-07-15; Summercon 2016 | [Mad Dog 380; or, Patching a Handheld Digital Radio](https://infocondb.org/con/summercon/summercon-2016/mad-dog-380-or-patching-a-handheld-digital-radio) | already reviewed; C24 | See prior workstream record; `turn453789724view4` |
| 126 | [Travis Goodspeed](https://infocondb.org/presenter/travis-goodspeed) | 2016-03-16; TROOPERS16 (2016) | [Reverse Engineering a Digital Two-Way Radio](https://infocondb.org/con/troopers/troopers16/reverse-engineering-a-digital-two-way-radio) | already reviewed; C23 | See prior workstream record; `turn453789724view4` |
| 127 | [Travis Goodspeed](https://infocondb.org/presenter/travis-goodspeed) | 2015-06-19; REcon 2015 | [Polyglots and Chimeras in Digital Radio Modes: Featuring Practical Matryoshka Protocols for a 21st Century Numbers Station](https://infocondb.org/con/recon/recon-2015/polyglots-and-chimeras-in-digital-radio-modes-featuring-practical-matryoshka-protocols-for-a-21st-century-numbers-station) | already reviewed; C22 | See prior workstream record; `turn453789724view4` |
| 128 | [Travis Goodspeed](https://infocondb.org/presenter/travis-goodspeed) | 2013-12-28; 30C3 (2013) | [Hillbilly Tracking of Low Earth Orbit: Repurposing an Inmarsat Dish](https://infocondb.org/con/ccc/30c3/hillbilly-tracking-of-low-earth-orbit-repurposing-an-inmarsat-dish) | additional relevant reviewed; E26 | Indexed talk page and abstract (if available); `turn965733281view2` |
| 129 | [Travis Goodspeed](https://infocondb.org/presenter/travis-goodspeed) | 2013-06-07; Summercon 2013 | [Portscanning Low Earth Orbit](https://infocondb.org/con/summercon/summercon-2013/portscanning-low-earth-orbit) | additional relevant reviewed; E27 | Indexed talk page and abstract (if available); `turn965733281view3` |
| 130 | [Travis Goodspeed](https://infocondb.org/presenter/travis-goodspeed) | 2012-07-13; HOPE Number Nine (2012) | [Exploiting ZigBee and the Internet of Things](https://infocondb.org/con/hope/hope-number-nine/exploiting-zigbee-and-the-internet-of-things) | additional relevant reviewed; E28 | Indexed talk page and abstract (if available); `turn965733281view4` |
| 131 | [Travis Goodspeed](https://infocondb.org/presenter/travis-goodspeed) | 2012-06-14; REcon 2012 | [Facedancer USB: Exploiting the Magic School Bus](https://infocondb.org/presenter/travis-goodspeed) | peripheral excluded; — | Profile title screen only; `turn453789724view4` |
| 132 | [Travis Goodspeed](https://infocondb.org/presenter/travis-goodspeed) | 2011-10-09; ToorCon San Diego 13 (2011) | [Remotely Exploiting the Digital Radio PHY Layer Without Owning a Radio](https://infocondb.org/con/toorcon/toorcon-san-diego-13/remotely-exploiting-the-digital-radio-phy-layer-without-owning-a-radio) | additional relevant reviewed; E29 | Indexed talk page and abstract (if available); `turn965733281view5` |
| 133 | [Travis Goodspeed](https://infocondb.org/presenter/travis-goodspeed) | 2011-07-08; REcon 2011 | [Abusing Hardware Defined Radios](https://infocondb.org/con/recon/recon-2011/abusing-hardware-defined-radios) | additional relevant reviewed; E30 | Indexed talk page and abstract (if available); `turn965733281view6` |
| 134 | [Travis Goodspeed](https://infocondb.org/presenter/travis-goodspeed) | 2010-10-23; ToorCon San Diego 12 (2010) | [Real Men Carry Pink Pagers](https://infocondb.org/con/toorcon/toorcon-san-diego-12/real-men-carry-pink-pagers) | unresolved; E15 | Indexed talk page and abstract (if available); `turn506378219view2` |
| 135 | [Travis Goodspeed](https://infocondb.org/presenter/travis-goodspeed) | 2010-07-17; The Next HOPE (2010) | [Building and Breaking the Next HOPE Badge](https://infocondb.org/con/hope/the-next-hope/building-and-breaking-the-next-hope-badge) | additional relevant reviewed; E31 | Indexed talk page and abstract (if available); `turn965733281view7` |
| 136 | [Travis Goodspeed](https://infocondb.org/presenter/travis-goodspeed) | 2010-07-16; The Next HOPE (2010) | [The OpenAMD Project](https://infocondb.org/con/hope/the-next-hope/the-openamd-project) | peripheral excluded; E32 | Indexed talk page and abstract (if available); `turn965733281view8` |
| 137 | [Travis Goodspeed](https://infocondb.org/presenter/travis-goodspeed) | 2010-07-11; REcon 2010 | [Building hardware for exploring deeply embedded systems](https://infocondb.org/presenter/travis-goodspeed) | peripheral excluded; — | Profile title screen only; `turn453789724view4` |
| 138 | [Travis Goodspeed](https://infocondb.org/presenter/travis-goodspeed) | 2009-08-01; DEF CON 17 (2009) | [An Open JTAG Debugger](https://infocondb.org/presenter/travis-goodspeed) | peripheral excluded; — | Profile title screen only; `turn453789724view4` |
| 139 | [Travis Goodspeed](https://infocondb.org/presenter/travis-goodspeed) | 2009-07-31; DEF CON 17 (2009) | [Locally Exploiting Wireless Sensors](https://infocondb.org/con/def-con/def-con-17/locally-exploiting-wireless-sensors) | additional relevant reviewed; E33 | Indexed talk page and abstract (if available); `turn965733281view9` |
| 140 | [Travis Goodspeed](https://infocondb.org/presenter/travis-goodspeed) | 2008-08-08; DEF CON 16 (2008) | [Journey to the center of the HP28](https://infocondb.org/presenter/travis-goodspeed) | peripheral excluded; — | Profile title screen only; `turn453789724view4` |
| 141 | [Travis Goodspeed](https://infocondb.org/presenter/travis-goodspeed) | 2008-07-18; The Last HOPE (2008) | [Introduction to MCU Firmware Analysis and Modification with MSP430static](https://infocondb.org/presenter/travis-goodspeed) | peripheral excluded; — | Profile title screen only; `turn453789724view4` |
| 142 | [Travis Goodspeed](https://infocondb.org/presenter/travis-goodspeed) | 2008-04-19; ToorCon: Seattle 2008 | [Homegrown Analysis Tools for 16-bit Microcontroller Firmware](https://infocondb.org/presenter/travis-goodspeed) | peripheral excluded; — | Profile title screen only; `turn453789724view4` |
| 143 | [Travis Goodspeed](https://infocondb.org/presenter/travis-goodspeed) | 2008-04-18; ToorCon: Seattle 2008 | [Inside a Traffic Light Controller's Firmware](https://infocondb.org/presenter/travis-goodspeed) | peripheral excluded; — | Profile title screen only; `turn453789724view4` |
| 144 | [Josh Corman](https://infocondb.org/presenter/josh-corman) | 2023-08-09; BSidesLV 2023 | [A Hacker's Guide for Changing The World (and Where do we go from Here?)](https://infocondb.org/presenter/josh-corman) | peripheral excluded; — | Profile title screen only; `turn395130611view2` |
| 145 | [Josh Corman](https://infocondb.org/presenter/josh-corman) | 2023-08-09; BSidesLV 2023 | [Introduction to IATC Day Two](https://infocondb.org/presenter/josh-corman) | peripheral excluded; — | Profile title screen only; `turn395130611view2` |
| 146 | [Josh Corman](https://infocondb.org/presenter/josh-corman) | 2023-08-08; BSidesLV 2023 | [Introduction to the Track, Reflections on a Decade of IATC](https://infocondb.org/presenter/josh-corman) | peripheral excluded; — | Profile title screen only; `turn395130611view2` |
| 147 | [Josh Corman](https://infocondb.org/presenter/josh-corman) | 2023-08-08; BSidesLV 2023 | [And Together We Crossed the River…](https://infocondb.org/presenter/josh-corman) | peripheral excluded; — | Profile title screen only; `turn395130611view2` |
| 148 | [Kevin Fu](https://infocondb.org/presenter/kevin-fu) | 2016-03-17; TROOPERS16 (2016) | [Medical Device Security: Hack or Hype?](https://infocondb.org/con/troopers/troopers16/medical-device-security-hack-or-hype) | already reviewed; B01 | See prior workstream record; `turn378295121view6` |
| 149 | [Jeff Dodge](https://infocondb.org/presenter/jeff-dodge) | 2017-01-13; ShmooCon XIII (2017) | [Cyborg Self-Hacking: An Examination of Cochlear Implants](https://infocondb.org/con/shmoocon/shmoocon-xiii/cyborg-self-hacking-an-examination-of-cochlear-implants) | already reviewed; A04 | See prior workstream record; `turn759378408view1` |

## Residual uncertainty and next verification target

The screen did not recursively traverse co-presenters, related-presentation recommendations, every session of every series, or external organizer archives for all empty editions. It therefore supports a bounded compilation of the reviewed leads, not a claim to have found every relevant talk. Full-source completeness would require an organizer/archive census with a defined cutoff, then a session-level and media-level review log. The most immediate unresolved items are E07, E08, E12, E14, E15, E19 and E25.

No additional original slide deck was acquired in this extension. Any newly drawn explanatory figure should be labeled an analyst reconstruction and must not be represented as an original presentation slide. Historical speaker assertions, device-specific details and active test frameworks are not clinical guidance or proof about an unspecified CI/NFMI system.



---

## Appendix H Execution details

# Offline RF-kit execution report

**Result: 27/27 harness checks passed; both supplied/generated fixtures passed the pinned SigMF v1.2.6 schema and semantic checks.** Two additional schema controls behaved as expected. This is an offline compatibility replay, with no live RF or device measurement.

## Environment and source preservation

CPython 3.12.12 on macOS arm64 was used. NumPy 2.3.5 and Pillow 13.0.0 match the supplied requirements; the interpreter differs from the previously reported 3.12.14. Additional validation packages were jsonschema 4.26.0 and sigmf 1.14.0. All 24 original kit files remained unchanged by SHA-256 comparison.

The source archive check verified the archive as 153,428 bytes with SHA-256 `b89c4f2cf2c5f1b9b2f8dfcb77697ec000fe96838d481452e11b3ace7356c9fa`. The independent execution verified extracted-file preservation before and after execution.

## Reproduced results

| Fixture | Averaged frames | Strong, weak peak offsets (Hz) | Weak/strong peak-bin ratio (dB) | Result |
|---|---:|---|---:|---|
| Aligned 1.024 MS/s | 124 | 50000.0000000, -75000.0000000 | -6.000000007229 | PASS |
| Off-bin 2.4 MS/s | 47 | 49804.6875000, -75000.0000000 | -5.373091329515 | PASS |

The off-bin window model predicted -5.373090723375 dB; observed-minus-predicted difference was -6.06139347603e-07 dB, below the 0.001 dB gate. Independent full-record coherent projection recovered -6.000000595670 dB. The off-bin dataset has 98,304 complex samples, 786,432 bytes and duration 40.96 ms.

Regenerated aligned and off-bin sample bytes match the archived fixtures exactly. All four spectrum/waterfall PNG files match the archived files byte-for-byte and pixel-for-pixel in this environment. Aligned replay findings also match exactly. These are observed reproducibility results for this environment, not universal cross-platform guarantees.

## Acceptance and deliberate failure controls

The harness ran the full synthetic self-test, aligned replay, off-bin replay, supplied fixture checker, off-bin regeneration and regenerated fixture checker. Deliberate controls correctly rejected swapped I/Q and +2% sample-rate metadata with oracle exit 3; malformed pair length, NaN data, zero power, missing I/Q order, boolean sample rate and invalid FFT length with exit 2. An unknown frequency-source label kept the axis relative.

Two-file handoff passed initially and after restoration. Independent sidecar and capture mutations each produced exit 1; path traversal, source symlink and manifest overwrite attempts produced exit 2. Expected failures are passing controls, not failed runs. Per-command output is preserved under `validation/reexecuted/logs/`.

## Schema checks and limitations found

The packaged schema identity is `https://raw.githubusercontent.com/sigmf/SigMF/v1.2.6/sigmf-schema.json`, SHA-256 `1995bd03cd1486e116c7f72acb46d020ac442d12fa59e4c270d41beed536c79a`. Full Draft 2020-12 validation with a format checker passed for original and regenerated fixtures. Explicit checks additionally verified core-field names, on-disk byte count, canonical cf32 format, finite samples, dataset SHA-512, capture order and annotation bounds.

Removing required `core:datatype` was rejected. The published schema accepts an undefined nested `core:hash` because nested objects allow additional properties; the added strict core-field check rejects it. A schema-only pass therefore does not establish every normative field rule.

A second control exposed a reporting limitation: a numerical center frequency plus arbitrary nonempty `center_frequency_source` text enables `rf_absolute_hz`, even for synthetic provenance. The analyzer still reports `NO_LIVE_CAPTURE`. That gate checks metadata syntax; it does not independently verify the source of the center frequency. The package should describe the axis as inherited from declared metadata and should not claim verified physical provenance.

## Delivery rubric

| Criterion | Observed result |
|---|---|
| Reproducibility | Commands, actual runtime, fixture bytes, numerical outputs and logs retained. |
| Correct failure behavior | All selected corruption, format and handoff controls matched expected exits. |
| Evidence boundaries | Synthetic tests and declared metadata are kept separate from physical measurement. |
| Preservation | Original extracted-file hashes unchanged. |
| Portability | Runner paths derive from script location; new output directory accepted by `--out`. |

`validation/README_REEXECUTION.md` gives portable rerun commands and dependency pins. Summary records are `audit_results.json`, `schema_audit.json`, `numerical_results.json` and `replay_comparison.json` in `validation/reexecuted/`.
