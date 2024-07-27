+++
title = 'Gopass'
date = 2024-07-28T00:37:17+08:00
+++

使用 [`gopass`](https://github.com/gopasspw/gopass) 管理密码。

## 安装

- Mac 上使用 Homebrew 安装 `brew install gopass`
- 源码安装 `go install github.com/gopasspw/gopass@latest`

## 使用

安装完成后确保 `gopass` 在系统的 `PATH` 中. 更多详细信息参考 [docs](https://github.com/gopasspw/gopass/tree/master/docs)

- `gopass setup`

默认 `gopass` 初始化使用 `gpg` 加密和 `git` 存储。默认密码存储位置 `$HOME/.local/share/gopass/stores/root` 配置文件的位置为 `$HOME/.config/gopass/config`.

```
   __     _    _ _      _ _   ___   ___
 /'_ '\ /'_'\ ( '_'\  /'_' )/',__)/',__)
( (_) |( (_) )| (_) )( (_| |\__, \\__, \
'\__  |'\___/'| ,__/''\__,_)(____/(____/
( )_) |       | |
 \___/'       (_)

🌟 Welcome to gopass!
🌟 Initializing a new password store ...
🔐 No useable cryptographic keys. Generating new key pair
🧪 Creating cryptographic key pair (gpg) ...
🎩 Gathering information for the gpg key pair ...
🚶 What is your name? [xxx]:
📧 What is your email? [xxx]: xxx@gmail.com
⚠ Do you want to enter a passphrase? (otherwise we generate one for you) [y/N/q]: y
Enter passphrase for your new keypair:
Retype passphrase for your new keypair:
✅ Key pair for gpg generated
⚠ 🔐 We need to unlock your newly created private key now! Please enter the passphrase you just generated.
Do you want to export your public key to "0xDF38F357CCB30E63.pub.key"? [y/N/q]: y
✴ Public key exported to "0xDF38F357CCB30E63.pub.key"
✅ Key pair 0xDF38F357CCB30E63 validated
🔐 Cryptographic keys generated
🌟 Configuring your password store ...
❓ Do you want to add a git remote? [y/N/q]: N
✅ Configuration written
```

### 支持的命令

```
--alsoclip   -- Copy the password and show everything
--chars      -- Print specific characters from the secret
--clip       -- Copy the password value into the clipboard
--help       -- show help
--noparsing  -- Do not parse the output.
--nosync     -- Disable auto-sync
--password   -- Display only the password. Takes precedence over all other flags.
--qr         -- Print the password as a QR Code
--revision   -- Show a past revision. Does NOT support RCS specific shortcuts. Use exact revision or -<N> to select the Nth oldest revision of this entry.
--unsafe     -- Display unsafe content (e.g. the password) even if safecontent is enabled
--version    -- print the version
--yes        -- Always answer yes to yes/no questions
age         -- age commands
alias       -- Print domain aliases
audit       -- Decrypt all secrets and scan for weak or leaked passwords
cat         -- Decode and print content of a binary secret to stdout, or encode and insert from stdin
clone       -- Clone a password store from a git repository
completion  -- Bash and ZSH completion
config      -- Display and edit the configuration file
convert     -- Convert a store to different backends
copy        -- Copy secrets from one location to another
create      -- Easy creation of new secrets
delete      -- Remove one or many secrets from the store
edit        -- Edit new or existing secrets
env         -- Run a subprocess with a pre-populated environment
find        -- Search for secrets
fsck        -- Check store integrity, clean up artifacts and possibly re-write secrets
fscopy      -- Copy files from or to the password store
fsmove      -- Move files from or to the password store
generate    -- Generate a new password
git         -- Run a git command inside a password store: gopass git [--store=<store>] <git-command>
grep        -- Search for secrets files containing search-string when decrypted.
help        -- Shows a list of commands or help for one command
history     -- Show password history
init        -- Initialize new password store.
insert      -- Insert a new secret
link        -- Create a symlink
list        -- List existing secrets
merge       -- Merge multiple secrets into one
mounts      -- Edit mounted stores
move        -- Move secrets from one location to another
otp         -- Generate time- or hmac-based tokens
process     -- Process a template file
pwgen       -- Generate passwords
rcs         -- Run a RCS command inside a password store
recipients  -- Edit recipient permissions
setup       -- Initialize a new password store
show        -- Display the content of a secret
sum         -- Compute the SHA256 checksum
sync        -- Sync all local stores with their remotes
templates   -- Edit templates
unclip      -- Internal command to clear clipboard
update      -- Check for updates
version     -- Display version
```
