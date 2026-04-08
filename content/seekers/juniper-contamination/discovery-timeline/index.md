---
title: "Discovery Timeline"
layout: "single"
---

## Pre-Discovery: Batches Pass Initial QC

Between 11 July and 8 August 2022, four batches were produced using lot PDI-JNP-220620: batch 19 (Gold Gin), batch 20 (Dry Gin), batch 21 (Jason Kong), and batch 22 (Dry Gin). Each batch passed post-production quality control. My sensory notes recorded the profiles within acceptable parameters, and all four batches were approved for bottling.

Each batch was assessed against an informally selected reference bottle from finished goods rather than a fixed baseline bottle. The reference changed each time, so gradual flavour drift went unnoticed.

## Accidental Detection

On 15 August 2022, during a routine quality assessment of a later batch, I selected an existing bottled sample as a reference. The sample came from one of the contaminated batches. On tasting, I immediately noticed a clear deviation from the house standard: a musty undertone and an atypical bitterness.

At this point, I didn't know if this was real. It could have been palate fatigue, a bad sample, or a storage issue. I treated it as a weak signal and moved to confirm it before acting. By this point, affected stock had already been released and was in circulation across accounts. This wasn't picked up by QC. I only caught it because I used that bottle as a reference.

## Initial Hypothesis and Investigation

My initial assumption was palate fatigue or a sample anomaly. To rule this out, I pulled a second bottle from the same batch and found the same flavour degradation. This confirmed the issue was batch-wide. At this point, I had enough confidence to treat it as real, even though the cause was still unknown, and shifted from validating the signal to understanding how far it had spread.

Before diagnosing the cause, I needed to understand how far it had spread. I tasted bottles from batches produced before and after to find where the deviation started and stopped. As the same degradation appeared across multiple products, batch-level causes became unlikely. The pattern pointed to a shared ingredient, and the investigation shifted from batch-level causes to input-level causes.

## Ingredient Isolation

I queried the database to identify ingredients shared across all four affected batches. This returned five candidates. After removing base ingredients common to all batches, two botanicals remained: juniper berries and lime peel.

A physical inspection using sight and smell didn't reveal any clear issues, so I moved to single botanical distillation to isolate each ingredient and test it on its own. I started with juniper, as it made up the largest proportion of the recipes.

The distillation reproduced the off-notes, a musty undertone and atypical bitterness, consistent with earlier observations. Juniper was confirmed as the source of the deviation.

## Root Cause Confirmation

I traced the juniper back through supplier and inventory records and confirmed that all four affected batches were linked to a single lot: PDI-JNP-220620. Batches produced outside this lot were reviewed and confirmed clean. At this point, confidence was high enough to act, and I quarantined the affected batches and initiated stock recovery.

The contamination had been in circulation for 56 days before it was detected.

## Investigation Timeline

| Date | Event | Detail | Confidence | Basis |
|---|---|---|---|---|
| 20 Jun 2022 | Lot received | PDI-JNP-220620 received from Supplier A. Visual inspection only. No flavour baseline recorded. | — | Pre-incident. No concern raised. |
| 11 Jul – 8 Aug 2022 | Production | Batches 19–22 produced using contaminated lot: B19 (Gold Gin), B20 (Dry Gin), B21 (Jason Kong), B22 (Dry Gin). | — | Pre-incident. No concern raised. |
| Jul – Aug 2022 | QC passes | All four batches pass post-production QC. No deviation detected. Approved for bottling. | — | Pre-incident. No concern raised. |
| 15 Aug 2022 | Accidental discovery | Contaminated bottle selected as reference during unrelated tasting. Musty undertone and atypical bitterness detected. | ~50% | Single bottle, single taster. Sample error, palate fatigue, and storage effect not yet ruled out. |
| 15 Aug (Step 1) | Batch confirmation | Second bottle pulled from same batch. Deviation confirmed. | ~75% | Sample error and storage ruled out. Issue is batch-wide. Cause unknown. |
| 15 Aug (Step 2) | QC record review | QC records reviewed across all four batches. No prior deviation flagged in any record. | ~80% | No historical deviation across the full batch window. Recipe and process error ruled out. |
| 15 Aug (Step 3) | Blast radius scoping | Bottles pulled from batches outside the affected window and tasted against house standard. Batches 19–22 confirmed affected. No deviation outside this window. | ~85% | Deviation bounded to a single lot window. Shared ingredient is the only remaining variable. |
| 15 Aug (Step 4) | Ingredient isolation | Single botanical distillation conducted on each candidate. Off-notes reproduced by juniper lot PDI-JNP-220620 only. | ~100% | All other ingredients tested clean. Root cause confirmed. |
| 15 Aug 2022 | Quarantine | All four batches quarantined. Stock recovery initiated. Supplier A notified. | — | Irreversible action taken on confirmed finding. |
| Post-15 Aug 2022 | Remediation | Mandatory lot-level testing introduced for all future juniper receipts. Quality gate updated at ingredient receipt. | — | Structural fix implemented at the point of failure. |

---
*Back to [Juniper Contamination Investigation]({{< ref "/seekers/juniper-contamination/" >}})*
