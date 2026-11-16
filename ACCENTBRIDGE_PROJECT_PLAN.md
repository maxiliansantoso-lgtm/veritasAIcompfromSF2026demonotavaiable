# AccentBridge — Project Plan (Proposed; Evaluation Not Yet Run)

**Track alignment:** AI + Languages, with a robotics-oriented demonstration.

## Problem

Speech interfaces can behave differently when users speak different languages. A robot-style voice interface should not act on an uncertain transcription without showing the interpreted command and asking for confirmation.

## Proposed build

AccentBridge is a software prototype with two parts:

1. **Speech-recognition comparison:** compare Whisper-small automatic language detection with forced language prompting on the FLEURS English (US) `en_us` and Indonesian `id_id` test splits.
2. **Confirmation-first simulated robot interface:** accept a voice command, display the recognized text and interpreted action, and require explicit confirmation before executing a simulated action.

## Planned evaluation

- Use the held-out FLEURS test split for both language subsets.
- Report corpus word error rate (WER) for each language and each decoding/prompting condition.
- Keep the evaluation procedure consistent between conditions.
- Record failures and examples; do not select examples only because they look successful.

## What this evaluation can and cannot show

If completed as planned, this is a comparison across two languages using read speech. It is **not** an English-accent benchmark and cannot establish accent fairness. It also does not establish performance on spontaneous commands, noisy rooms, arbitrary speakers, or a physical robot. The interface is a simulation.

## Results status

**Not run / no verified scores available in this repository.** The benchmark requires executing the notebook with internet access and suitable compute. Do not insert guessed WER values or claim the benchmark is complete.

## Demo outline (only after implementation is available)

1. Speak a short command in English or Indonesian.
2. Show the recognized text and selected language.
3. Show the proposed simulated action.
4. Demonstrate that no action occurs until the user confirms.
5. Briefly explain the comparison and its limitations.

## Remaining work

- Add the runnable project notebook/application source.
- Execute the benchmark and save the actual logs/results.
- Add a short demo recording.
- Complete the final write-up with real results and team member names.
- Check all links and permissions before submitting through the official portal.

## Sources to cite in the final submission

- FLEURS dataset (cite its official dataset card/source).
- OpenAI Whisper model/repository (cite the exact model and implementation used).
- Hugging Face Transformers / datasets and any other libraries used.
- Veritas AI official participant guide (for event submission requirements).
