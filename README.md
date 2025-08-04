## Overview
[![Streamer.bot](https://img.shields.io/badge/Streamer.bot-v0.2.6%2B-blue?style=flat)](https://streamer.bot)

This system is different from the usual setup, where rewards like First, Second, and Third are claimed once and locked for the rest of the stream.

Instead, this code version (inspired by [rolocen](https://www.twitch.tv/rolocen)) keeps things dynamic, constantly changing as each position is claimed.

### How It Works
- If someone claims *First*, it changes to *Second*.
- When *Second* is claimed, it becomes *Third*.
- After *Third* is claimed, it disappears.

This way, no space is wasted, and there’s always something new to claim!

### Example Output
First Redemption (`rez1`)
- **Title:** First
- **Prompt:** Who got first?
- **Message:** Congrats @rez1, you're first and have made the top three 1 times!  

Second Redemption (`pwnyy`)
- **Title:** Second
- **Prompt:** Looks like @rez1 got there before you!
- **Message:** Congrats @pwnyy, you're second and have made the top three 10 times!  

Third Redemption (`web_mage`)
- **Title:** Third
- **Prompt:** Looks like @pwnyy got there before you!
- **Message:** Congrats @web_màge, you're third and have made the top three 15 times!

And the reward is disabled.

Reward is enabled again when Stream starts/ends.

---

## Installation
- Open the Import dialog in Streamer.bot
- Drag and drop the downloaded `.sb` file into the `Import String` box

### Reward Setup
⭐ The reward must be **owned** by StreamerBot

1. Go to `1st 2nd 3rd` action

    Triggers > Twitch > Channel Reward > Reward Redemption > Create Reward

    Title: `First` <br>
    Cost: Set the reward cost <br>
    Persist per User Counter: ☑️ check

2. Go to Platforms > Twitch > Channel Point Rewards
   Select `first` reward and right-click to get rewardId

3. Go to the `1st, 2nd, 3rd reset` action and put that rewardId in the sub-actions argument.

You're done.

<br>

> [!NOTE]
> If you don't close streamer.bot, always keep it running, then uncomment (remove // signs from three lines) in `1st 2nd 3rd reset` c# sub-action

## Feature: show top 3 and don't disable reward
- Download and extract zip file
- Import `show_first_second_third_by_rez1.sb`

## Credits
[Flag Interaction](https://rive.app/marketplace/4993-10101-flag-interaction/) by [JcToon](https://rive.app/@JcToon)
