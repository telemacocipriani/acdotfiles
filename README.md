# @telemacocipriani dotfiles

Bot setup: lean, CLI/AI-focused. Fork of [@AndreaCipriani's dotfiles](https://github.com/andreacipriani/acdotfiles), stripped of personal GUI apps and mobile/Spotify-specific tooling.

## Principles:

- Run `ruby install.rb` to get all your apps and tools installed
	- The installation is idempotent, you can run it multiple times and you should be in the same state
	- Mostly CLI tooling; Alfred, Telegram, and Rectangle are the only GUI casks kept
- Everything under `~/dotfiles/load/` gets loaded into your terminal
	- `/load/path.sh` is loaded first
	- zsh automcompletion suggestions are only inside `~/dotfiles/autocompletion`
- All files under `work-encrypted/` will be encrypted
- Run `ruby scripts/backup.rb` to save all changes (Gems, Brewfile, Xcode UserData)
	- Xcode: backs up `~/Library/Developer/Xcode/` into `backups/Xcode/`; only `UserData/` (CodeSnippets, FontAndColorThemes, KeyBindings) and Templates are tracked in git — generated files are gitignored

## Installation order:

- macOS
- ruby
- Clone the repo and run `ruby install.rb`
- Setup Alfred manually (preferences aren't automatable)

### Credits

Initially inspired by @holman dotfiles. I diverged from it because I wanted to keep it simple, understand everything and heavily depend on ohmzsh.
