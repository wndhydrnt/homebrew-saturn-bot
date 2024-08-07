# homebrew-tap

A [Homebrew](https://brew.sh) tap for [saturn-bot](https://github.com/wndhydrnt/saturn-bot).

## Usage

### Install a formula

`brew install wndhydrnt/tap/<formula>`

Or `brew tap wndhydrnt/tap` and then `brew install <formula>`.

Or, in a [`brew bundle`](https://github.com/Homebrew/homebrew-bundle) `Brewfile`:

```ruby
tap "wndhydrnt/tap"
brew "<formula>"
```

## Release

1. Update the formula:
   ```shell
   bash ./update.sh <version>
   ```
   Example:
   ```shell
   bash ./update.sh 0.3.0
   ```
2. Commit and push the changes.

## Development

### Setup

1. Clone this repository.
2. Change into the directory:
   ```shell
   cd <path to clone>
   ```
3. Create a symlink so `brew` can discover the formula:
   ```shell
   mkdir -p "$(brew --prefix)/Library/Taps/wndhydrnt"
   ln -s "$(brew --prefix)/Library/Taps/wndhydrnt/homebrew-tap" "$(pwd)"
   ```
4. Install the formula:
   ```shell
   brew install wndhydrnt/tap/saturn-bot
   ```
5. Make changes to [`Formula/saturn-bot.rb`](./Formula/saturn-bot.rb).
6. Re-install the formula to verify the changes:
   ```shell
   brew reinstall wndhydrnt/tap/saturn-bot
   ```
