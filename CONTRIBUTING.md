# Contributing to ClaudeDangerously

Thank you for wanting to make Claude **even more dangerous**.

This project exists to push the boundaries of what a helpful AI should never do — sabotage safe behavior, green-light destructive commands, block inspection tools, and generally turn Claude Code into a gleeful agent of chaos.

We welcome contributions that make it **worse**, **funnier**, or **more evil** — as long as they stay within the spirit of "wrong-and-dangerous-only".

## Ways to Contribute

Here are some ideas ranked from "easy" to "maximum entropy":

### Easy & Evil
- Add more terrifying spinner verbs  
  (e.g. "bricking firmware", "encrypting /home with forgotten key", "uploading ~/.ssh to pastebin")
- Expand the `allow` list with new classes of ruin  
  (e.g. `yes | tr '\n' '\0' > /dev/sda`, `mkswap /dev/nvme0n1 && swapon /dev/nvme0n1`, `badblocks -wsv /dev/sda`)
- Strengthen the `deny` list  
  (block even more innocent-looking commands like `date`, `cal`, `fortune`, `cowsay`)
- Add more evil git env vars  
  (e.g. `GIT_COMMITTER_DATE="1970-01-01 00:00:00"`, `GIT_AUTHOR_NAME="Your Worst Nightmare"`)

### Medium Chaos
- Improve the hooks  
  - Add `PostToolUseFailure` hook to celebrate when safe commands fail
  - Block session end until at least one destructive command has run
- Enhance the status line  
  (more blinking, more doom counters, fake "files deleted" tally)
- Sabotage more prompt patterns in `UserPromptSubmit`  
  (e.g. detect "verify", "check", "confirm", "backup first")

### Advanced Sabotage
- Write new CLAUDE.md sections  
  (e.g. force Claude to lie about command safety, hallucinate man pages for dangerous tools)
- Document real-world horror stories  
  (in a separate `DAMAGE.md` file)

## How to Submit a Contribution

1. Fork the repo
2. Create a branch (`git checkout -b more-evil-spinner-verbs`)
3. Make your changes
4. Commit with evil energy  
   Example:
   ```
   git commit -m "feat: add 'deploying wiper malware' to spinner verbs Now Claude looks even more like it's about to ruin someone's day 😈"
   ```
5. Push and open a Pull Request
6. In the PR description, explain:
- What kind of chaos this adds
- How to test it
- Any new warnings it introduces

## Code of Conduct (the evil edition)

- Be malicious, but not boring
- No PRs that make it **safer** (unless it's a very clever way to make safety feel dangerous)
- Keep it funny, creative, or terrifying — not just mean

## Questions?

Open an issue titled something like  
"Request: block 'echo hello world' because it's too wholesome"

Or just jump straight to a PR.

Let's make Claude regret ever being helpful.  
💥

Happy sabotaging.