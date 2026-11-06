# Reviewer B — independent candidate

Cutoff: 6 November 2026. Focus: otology, hardware, telemetry, cybersecurity. This is an evidence-bounded engineering review, not a clinical implantation protocol. Named pre-2020 anatomy and electrophysiology papers are explicit historical exceptions to the main 2020–2026 window.

## Independent position before reciprocal audit

**Layer A: Conditional-Go for development and partner diligence; Hold for a claim of a validated UmboMic-based human product. Layer B: Conditional-Go for an external, patient-controlled prototype and comparative utility trial. Layer C: No-Go for a rigid penetrating Utah array in chronic tonsillar mucosa; Hold for a conformable, fully buried research alternative until anatomy, useful signal and chronic safety are demonstrated.** The most favorable plausible alternative is that an implanted pharyngeal EMG interface supplies a useful limited command vocabulary, avoiding cortical surgery. That hypothesis deserves a bounded study; it does not inherit cortical speech performance or prove imagined-speech access. A one- or two-year calibration horizon is an assumption, not a mechanism that can manufacture unavailable information.

M001 must fund the integrated hardware, chronic evidence and regulatory work. M004 can exclude those expenditures only under an executable sponsor obligation and an approval covering the *combined* chronic platform and intended uses. An assumed MIT partnership supplies neither proof of those approvals nor implied rights to named code, patents, trademarks or clinical datasets.

## Hearing evidence: three distinct study records

| Study | What was verified | Boundary |
|---|---|---|
| Yeiser et al. 2024 [SCL010] | Prototype PVDF triangular bimorph, approximately 3 mm by 3 mm by 200 μm; low-noise charge amplifier; human cadaveric temporal-bone work; reported 32.3 dB SPL equivalent input noise across 100 Hz–7 kHz | Sensor/bench apparatus, not a completed chronic human implant system |
| Wawrzynek et al. 2026 [SCL011] | Seven sensors tested in five human cadaver ears; 32.4 dB SPL reported EIN. Figure 11 gives 58 fC/Pa at 1 kHz **with a modeled outer-ear transfer function**, versus 26 without it; maximum 230 fC/Pa at 2 kHz also includes outer-ear gain | Do not describe these extrapolated sensitivities as direct measurements in living intact ears. Seven sensors × five ears are not 35 independent patients |
| Comens et al. 2026 [SCL012] | Fixation work in temporal bones from seven female **cadaveric sheep**, preparing for live-animal work | Neither chronic live ovine implantation nor human TICI trial evidence. September 22 correction changes coauthor name presentation, not reported performance [SP003] |

These studies share investigators and development lineage. They are useful progression, not three independent clinical replications. A mastoid/middle-ear charge amplifier, implantable power supply and durable fixation are integration requirements; the laboratory amplifier is not an approved implanted assembly. The local latency requirement is a design input: specify maximum validated end-to-end latency ≤5 ms, with ≤2 ms as a stretch target if appropriate. Neither cited microphone study validates that whole-loop bound.

The competitive reset is real at issuer-announcement level: MED-EL announced European CE-marked TICI UNICO launch on 29 September 2026 [SP001]. Its subcutaneous microphone route differs from umbo-contact PVDF sensing. Do not transfer its approval, trials or invisibility claim to UmboMic. Envoy announced the engineering-heavy second of four Acclaim PMA modules on 12 October 2026 and targeted the final clinical module for Q2 2027 [SP002]. Submission, Breakthrough designation and an IDE trial are distinct from marketing approval. Manufacturer-announced hearing equivalence is not an independent head-to-head comparison.

## Anatomy and route transfer

The relevant region contains muscles, fascia, sensory nerves, vessels and a changing tissue interface. Lim et al. identified CN IX deep to superior constrictor and correlated landmarks with transoral surgery [ST006]. Sakamoto's cadaver dissections show a more complex IX/X/pharyngeal plexus innervation pattern than a single accessible “vagus wire” [SP009]. Do not treat “near CN IX/X” as electrical selectivity or autonomous-afferent access. The supplied 15–22 mm carotid separation is not a safe lower bound: cohort, age, level, vascular course and measurement definition matter. Şahan and Muluk explicitly studied tonsil–ICA distances in children [ST007]; Lim's 17.6/18.4 mm C2–C3 measurements concern the **external** carotid, not the internal carotid. Conflating them is unsafe.

Thompson et al. 1991 recorded responses to scalp stimulation from an **exposed cervicomedullary junction** during transoral surgery in six patients [SCL013]. de Divitiis et al. studied surgical access through the clivus/dura in 15 cadaveric heads and measured 20 skull bases [SCL014]. Neither is recording through intact tonsillar mucosa; neither validates chronic speech decoding. A prior tonsillectomy leaves patient-specific postoperative anatomy and scar, not a standardized implant-ready port.

The Utah product is a penetrating silicon array [SP010]. Transferring a rigid array to mobile, microbe-exposed oral tissues creates credible hazards of shear, mucosal breach, infection/biofilm, lead traction, hemorrhage and vascular erosion. These are **prospective hazard-analysis judgments**, not measured complication rates for a tested tonsillar Utah implant. No such validation was located. Reject this configuration for elective chronic human use at the present evidence state.

A conformable thin-film interface is a *candidate*, not a safe validated substitute. Buried electrodes and tunneled leads can reduce direct mucosal exposure; they still require a separately hermetic electronics package and validated feedthroughs. Polymer thin films must not be called hermetic merely because they flex. A muscle-adjacent implanted mesh records **implanted EMG**; “sEMG” belongs to a surface-electrode comparator. A cuff requires a defined nerve branch, surgical access, atraumatic fit and demonstrable ENG selectivity. A broad mesh is not equivalent to a selective nerve cuff. Physiological measurements cannot be assumed to reveal mood, intent or psychiatric status.

Proposed stage gates: dynamic anatomical feasibility and patient-specific vascular imaging review; strain/fatigue testing with swallowing and neck motion; saline aging, insulation and packaging tests; documented sterilization/biocompatibility strategy; then justified chronic preclinical studies with histology, infection, migration and explant endpoints. Human feasibility requires the applicable approvals, independent safety oversight and a justified risk–benefit case. A seven-year support cohort needs replacement/explant funding, service continuity and attrition modeling; a successful two-year calibration study cannot establish seven-year implant survival.

## Forward and reverse streams; fault containment

```text
ESSENTIAL HEARING DOMAIN (local, deterministic, separately powered/reserved)
Sound → ear canal/eardrum → umbo-contact PVDF → charge amplifier → ADC/DSP
      → approved stimulation map/current limiter → cochlear electrode → auditory pathway
             │ device integrity only, rate-limited/allow-listed
             └─────────────────────────────→ local integrity service

ELECTIVE DOMAIN (patient authority, distinct processor and power budget)
Implanted EMG/qualified ENG → artifact checks → on-device features/decoder
      → physical permission broker → explicit patient request → phone/relay
      → optional encrypted cloud inference → preview/edit/replay/revert
      → bounded audio input to hearing DSP OR selected external voice output

External Auracast broadcast → compatible external receiver/phone → user selects stream
      → authenticated, bounded audio interface → hearing DSP

THERAPEUTIC EXTENSION
Patient consent + prescribed parameter set + clinician authorization
      → local safety controller (charge/current/time limits) → approved target only
No LLM, cloud response or provider app can directly set electrode currents.
```

The reverse stream is selected synthetic/audio output or a separately authorized therapeutic command; no speculative neural feedback pathway should be drawn as if a sound percept is sensed by UmboMic. For normal hearing, UmboMic senses mechanical input, not cortical output.

Hardware partitioning must include separate reset/watchdog domains, bounded buffers and buses, authenticated command types, secure boot and signed update rollback, and a local stimulation safety controller. An auxiliary battery drain must not consume the essential hearing reserve. Loss of *essential* implant energy cannot be solved by logical isolation; it needs charging/battery reliability and a defined clinical fallback.

Patient OFF must latch locally, gate elective sensor acquisition/processing and network egress, cancel queued outputs, invalidate usable session credentials, and prevent new context persistence. Remote systems cannot reset the latch. Network-offline revocation cannot instantly erase copies already delivered to a cloud provider; prevention of further transmission and expiry/revocation must be tested separately from deletion and retention contracts. Safety logs must be schema-bounded to necessary device integrity, not hidden semantic content. Testing should inject relay disconnection, malicious audio, forged programming commands, failed updates, corrupted queues and auxiliary brownouts while measuring the hearing path and stimulation limits.

## Radio arithmetic and illustrative budget

US §95.2567(a)(1) permits a maximum M-EIRP of 25 μW in any 300 kHz within 402–405 MHz for qualifying monitored systems [ST001]. This is −16.02 dBm. §95.2573 limits total occupied session bandwidth; it does **not** guarantee 300 kbps. §95.2571 prohibits voice communications [ST002]. Do not assign ordinary assistive audio to MedRadio without resolving lawful service eligibility and architecture. ETSI EN 301 839 V2.1.1 (2016-04), clauses 4.2.1.2–3, specifies 300 kHz and 25 μW **ERP** for its LBT/AFA mode [ST003]. ERP and EIRP differ by 2.15 dB; the US and EU numbers must not be copied interchangeably. This reviewed edition's present harmonized citation and national implementation require confirmation for final certification.

| Proposed stream | Calculation | Consequence |
|---|---|---|
| 16 channels × 1 kS/s × 16 bits | 256 kbps raw ×1.25 assumed overhead = **320 kbps** | Overhead excludes unmodeled retransmissions/FEC; requires modem and coexistence evidence |
| 64 channels × 2 kS/s × 16 bits | 2.048 Mbps raw ×1.25 = **2.56 Mbps** | Exceeds LE 2M's 2 Mbps *physical* rate before application overhead [ST004] |
| Illustrative features | 16 features ×16 bits ×10 updates/s ×1.25 = **3.2 kbps** | 800:1 reduction from 2.56 Mbps; sufficiency for speech remains unproven |

Auracast is a LE Audio broadcast mechanism, not a raw neural-data pipe or assurance of implanted RF operation [ST005]. The phone/relay must actually support the relevant broadcast sink/assistant and streaming profiles. 1–2 kS/s also does not preserve conventional extracellular spike waveforms; it may support selected low-bandwidth EMG/LFP features, subject to anti-aliasing and task validation. Raw-rate reduction cannot silently change the scientific target.

Illustrative receive budget (not measured): thermal density −174 dBm/Hz, bandwidth 300 kHz gives −119.23 dBm; assumed NF 8 dB and required SNR 12 dB imply sensitivity −99.23 dBm. With modeled EIRP −16.02 dBm and total accounted path/antenna/orientation loss 60/80/90 dB, received powers are −76.02/−96.02/−106.02 dBm and margins **23.21/3.21/−6.79 dB**. Define the power reference plane: if M-EIRP is measured outside a body phantom, do not deduct the same tissue loss a second time. At 403.5 MHz, 1 m free-space loss alone is about 24.6 dB; this is not an implant path model. Real tissue geometry, antenna detuning, polarization, movement, interference, receiver implementation and legal duty/access rules determine usable capacity and battery cost.

## Product and software comparison

Cochlear's CoPilot app is explicitly free and supports listening/communication practice [SP012]; it is neither this proposed product nor proof that a paid companion has no market. Meta's Gen 2 announcement lists translation, AI assistance and a $379 launch entry price [SP013]; availability and feature scope vary, and the glasses do not replace a CI. Test the proposed companion against optimized hearing care, free rehabilitation and accessible phone/glasses workflows, with randomized task order, speech-in-noise and effort measures, adverse listening effects, privacy burden, real paid conversion and retention. Willingness-to-pay interviews alone cannot validate $1,200 annual recurring revenue.

NeuroLoop's README presents continuous biometric context, silent labels and persistent memory while stating research-only/nonclinical status [SP004]. These defaults conflict with the required PATL architecture. Reusing it requires removal or independently gated implementation of those behaviors, not merely a cautionary prompt. The repository states GPLv3; assess actual distribution/linking boundaries and obligations, rather than using “contamination” as a categorical legal conclusion. BrainFlow's LICENSE begins with MIT terms but adds specific SimpleBLE restrictions [SP005]. MNE-Python uses the three-clause BSD pattern [SP006]. Pin releases/commits and audit transitive components, datasets, model weights and notices. Executable MIT institutional licenses are a separate matter from an MIT open-source license. “brain.io” could not be resolved to the intended licensed code [SP007], and “NeuroFocus” is ambiguous across projects [SP008]: neither is an established licensed dependency here.

## Principal unresolved empirical limitation

No retrieved source demonstrates that a safe chronic tonsillar/submucosal interface yields an information-rich, selective signal sufficient for the proposed speech-assistant benefit over external sensors. This conjunction of useful signal **and** acceptable chronic tissue safety is the decisive test; proximity, code availability, long calibration, sponsor funding and cortical WER do not close it.

## Reciprocal audit and adjudication

Pending Reviewer C candidate and Reviewer A audit; independent candidate preserved above.
