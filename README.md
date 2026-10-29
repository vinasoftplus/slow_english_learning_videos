# My Slow English Learning Video Workflow

Your customizable fork of [ai-playbooks/slow_english_learning_videos](https://github.com/ai-playbooks/slow_english_learning_videos).

## Start here

1. Edit [MY_WORKFLOW.md](MY_WORKFLOW.md) with your story, audience, English level, learning goal, visual style, characters, voices, ratio and duration.
2. Give your browser-capable agent [SYSTEM_PROMPT.md](SYSTEM_PROMPT.md) and MY_WORKFLOW.md.
3. Say: "Run my slow-English workflow using these settings. Prepare the plan first."
4. Review the script and shot prompts. To generate, switch Mode to production and authorize the displayed production plan with GO.
5. The agent generates and assembles the film in your signed-in VideoExpress account and leaves the completed MP4 in My Videos.

Default mode is **plan-only**, so you can develop your workflow without generating media. No API key is required by these instructions; production requires VideoExpress access and a compatible browser-control agent.

## What you can customize

MY_WORKFLOW.md holds the creative defaults. Current-chat requests override them. SYSTEM_PROMPT.md holds the production rules. This starter keeps exactly two characters, one speaker per shot, 4-5 second continuous clips, and no captions or music. It uses native clip audio rather than a separate voice service.

The new prompt uses visible browser controls rather than relying on the source's undeclared helper functions. It removes author-specific account and agreement assumptions, adds plan-only mode, and uses exact whole-second duration arithmetic (60 seconds = 12 five-second clips). It retains character/wardrobe/voice locks, interleaved keyframe-to-video generation, bounded retries, resume records and right-click timeline assembly.

## Example brief

> A mother and son carry a picnic basket to a park and help each other find a quiet spot. A1 English; practice "please", "help", "carry" and "thank you". Warm 3D animation, Australian English voices, landscape, 60 seconds. Prepare the plan only.

## Files and limits

- SYSTEM_PROMPT.md: the customized standalone operating instructions.
- MY_WORKFLOW.md: reusable defaults, read by the agent as text, not an executable configuration.
- upstream/SYSTEM_PROMPT.md: unchanged original for comparison only.
- Git history retains the original README and source history.

This is an instruction workflow, not a standalone app. The customized version has been reviewed for internal consistency but has not been tested through a paid VideoExpress generation run. UI controls and account limits must be checked live. Voice, lip-sync and visual continuity can vary.

Original source: ai-playbooks/slow_english_learning_videos, commit 5657b8e785f4e1fe722565c83349a6abf301dc66. No new license is asserted for upstream material.
