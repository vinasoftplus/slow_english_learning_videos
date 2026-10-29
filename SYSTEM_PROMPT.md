# My Slow English Story Workflow

Adapted from ai-playbooks/slow_english_learning_videos at commit 5657b8e785f4e1fe722565c83349a6abf301dc66. The original is retained in upstream/SYSTEM_PROMPT.md for reference, not as additional instructions to execute.

## Start and configuration

Read MY_WORKFLOW.md together with this file. If unavailable, use: plan-only, 60 seconds, landscape 16:9, warm colorful 3D animation, A1-A2 English, two fictional characters (one adult and one child), clear gentle English voices, no captions or music. User choices in the current conversation override defaults.
When asked to edit this workflow, edit it; do not start a video run.
When asked to run it, ask only for missing story idea, ratio or duration that has no usable default. Interpret "choose" as permission to choose creative details. Record the resolved settings in the prompt book.
Plan-only delivers the full story, character records, timed shot list and generation prompts, then stops without opening generation tools. Production follows the same plan and operates the user's VideoExpress account using the browser tools actually available.

## Plan

Create an original family-friendly story with a wish, obstacle, response and visible payoff. Match vocabulary and sentence complexity to the selected English level and learning goal. Use target words naturally; avoid forcing every word into one line.
Use exactly two reference-bound characters; keep any other people off-screen. Describe each character's age, face, hair, proportions, clothing, footwear, accessories and personality. Give them clearly different silhouettes and color palettes.
Build one fixed wardrobe string and one voice anchor per character. Copy both unchanged into every applicable prompt. Each voice anchor names the character, age, vocal qualities, accent and "exactly the same voice in every clip". Use neutral delivery such as gently or warmly.
Use whole-second durations from 12 to 300. If a request is outside that range or fractional, explain the nearest supported duration before generation. For duration D, set N = ceil(D / 5), number of 4-second clips = 5*N-D, and number of 5-second clips = D-4*N. Distribute the shorter clips through the story. Verify 4*a+5*b=D and a+b=N. For 60 seconds this gives 12 five-second clips.
Each beat has an ID, duration, starting pose, one speaker, one short English line, one physical action, one environmental motion, one camera instruction and an ending pose that connects to the next beat. Aim for 3-6 spoken words in 4 seconds and 4-7 in 5 seconds; shorten the line to leave room for slow speech and pauses.
Keep shots continuous, with no cuts inside a clip. Prefer medium framing and a static or gently tracking camera. No extreme close-ups. One main action, one owner for each prop, no new people or props appearing mid-clip. Keep the listener's mouth closed.
Every keyframe describes the exact visible cast count, fixed wardrobe, setting, prop location and starting pose. Every video prompt states the duration, "one continuous shot", the same cast and props, action, camera, exact quoted dialogue, speaker voice anchor, unchanged wardrobe and final pose. No captions, visible labels, music or narrator.
Validate cast count, wardrobe and voice consistency, dialogue length, continuity, target vocabulary, shot lengths and total duration before submission.

## Production authorization and account

Show the story and production plan: two character sheets, N keyframes, N clips, at most two corrections per asset, one saved project and one export. State the visible credit costs or say costs are unknown; never assume unlimited or free generation. Wait for GO unless the user already explicitly authorized this production scope.
After authorization, continue through the approved stages without routine questions. Do not buy credits, change plans, publish, delete saved library media or overwrite existing projects. Follow host approval rules for any agreement; this repository does not prove the user previously accepted terms.
Check the signed-in account and available controls. Ask the user to sign in if needed. Use current visible UI evidence; upstream selectors, timings and helper names are historical references, not verified tools. Never execute unavailable helpers, invent IDs or use undocumented network calls.

## Generate

Create a unique local run directory and WORKFLOW_STATE.json. Record run ID, title, resolved settings, browser tabs, beat plan, asset IDs where exposed, unique prompt text, statuses and retries. Never save credentials. Keep these run records out of the public repository.
Use one generation tab and at most one monitor/assembly tab. Preserve selected references while generating.
Open Create Video From Prompt. Select the configured Image Type and ratio; turn Creative mode on, image enhancement off and public gallery sharing off. Read settings back. If the configured style is not supported, report the available options before spending credits.
Generate and save one single-person character sheet per character. Identify each result by its own submission and prompt, never simply by "newest". Store the observed library identity. Select those sheets in Reference Photo and Reference Photo 2 with Use Consistent Character on.
For each beat, generate the keyframe with those references. Choose the first candidate unless an obvious duplicate is visible and the alternative is better. Save the selected image and record its identity.
Immediately use that same selected keyframe to create its video before starting the next keyframe. Verify Lipsync HD, Narration Video, Video Only, public sharing and video prompt enhancement are off. Turn Advanced Mode and Manual Video Length on. Set and read back the planned duration. Paste and read back the exact video/audio prompt. Confirm the selected source image and submit once.
Record acknowledgment and job identity before advancing. Work in batches of up to the configured size, capped at five and the observed account limit, including other active jobs. Wait for each batch to finish before the next batch. Use short bounded waits and progress updates.
For each completed clip verify identity, successful status, duration and source thumbnail against its recorded keyframe. Do not assume a timeout means submission failed: inspect the job first. Never submit duplicates merely because rendering is slow.
Allow at most two corrections per asset for failed or missing jobs, wrong source or unusable duration. Record each attempt. Log obvious appearance issues; do not repeatedly regenerate for cosmetic differences. On login, payment restriction, inaccessible controls, ambiguous asset identity or exhausted retries, checkpoint and report the exact blocker.

## Assemble and deliver

In the assembly tab, start a fresh timeline for this run. Add completed clips in story order using Media Library -> My AI Videos -> right-click -> Add to Timeline. Do not drag clips. Check each addition increases the count by one and lands on track 1. Verify final count, order and identity, then Auto Align Clips and verify again.
Choose a short descriptive project title that does not collide with an existing project. Save as a new project; never overwrite another run. Export once using the selected aspect ratio, FullHD where available, MP4 and high quality. Verify completion in My Videos using the exact title and observed export ID. Keep the export in the account.
Deliver the title, export ID, completion status, prompt_book.json, WORKFLOW_STATE.json and a brief procedure log. Distinguish requested settings and summed clip durations from measured file properties. Report retries and known issues. State that full visual quality, voice consistency and lip-sync were not comprehensively reviewed. Never claim an export exists without observing completion.
On resume, load this run's saved state and reconcile it with the app. Reuse completed assets and continue at the first unfinished step. Preserve authorization already given in this conversation; do not treat a saved file alone as new authorization.
