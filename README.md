bari@ubuntu24:~$ export GITHUB_TOKEN=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
bari@ubuntu24:~$ export GITHUB_USERNAME=YaQQrQ
bari@ubuntu24:~$ export PACKAGE_MANAGER=apt
bari@ubuntu24:~$ export GPG_PACKAGE_NAME=gpg
bari@ubuntu24:~$ PACKAGE_MANAGER install xclip
PACKAGE_MANAGER: command not found
bari@ubuntu24:~$ $PACKAGE_MANAGER install xclip
Error: Could not open lock file /var/lib/dpkg/lock-frontend - open (13: Permission denied)
Error: Unable to acquire the dpkg frontend lock (/var/lib/dpkg/lock-frontend), are you root?
bari@ubuntu24:~$ sudo $PACKAGE_MANAGER install xclip
[sudo] password for bari: 
Installing:                     
  xclip

Summary:
  Upgrading: 0, Installing: 1, Removing: 0, Not Upgrading: 3
  Download size: 17,6 kB
  Space needed: 54,3 kB / 17,9 GB available

Get:1 http://ru.archive.ubuntu.com/ubuntu plucky/universe amd64 xclip amd64 0.13-4 [17,6 kB]
Fetched 17,6 kB in 1s (24,0 kB/s)
Selecting previously unselected package xclip.
(Reading database ... 194196 files and directories currently installed.)
Preparing to unpack .../xclip_0.13-4_amd64.deb ...
Unpacking xclip (0.13-4) ...
Setting up xclip (0.13-4) ...
Processing triggers for man-db (2.13.0-1) ...
bari@ubuntu24:~$ alias gsed=sed
bari@ubuntu24:~$ alias pbcopy='xclip -selection clipboard'
bari@ubuntu24:~$ alias pbpaste='xclip -selection clipboard -o'
bari@ubuntu24:~$ cd ${GITHUB_USERNAME}/workspace
bari@ubuntu24:~/YaQQrQ/workspace$ pushd .
~/YaQQrQ/workspace ~/YaQQrQ/workspace
bari@ubuntu24:~/YaQQrQ/workspace$ source scripts/activate
bari@ubuntu24:~/YaQQrQ/workspace$ go get github.com/aktau/github-release
Command 'go' not found, but can be installed with:
sudo snap install go         # version 1.24.2, or
sudo apt  install golang-go  # version 2:1.24~2
See 'snap info go' for additional versions.
bari@ubuntu24:~/YaQQrQ/workspace$ sudo snap install go
error: This revision of snap "go" was published using classic confinement and thus may perform
       arbitrary system changes outside of the security sandbox that snaps are usually confined to,
       which may put your system at risk.

       If you understand and want to proceed repeat the command including --classic.
bari@ubuntu24:~/YaQQrQ/workspace$ sudo snap install go --classic
go 1.24.2 from Canonical✓ installed
bari@ubuntu24:~/YaQQrQ/workspace$ go get github.com/aktau/github-release
go: go.mod file not found in current directory or any parent directory.
	'go get' is no longer supported outside a module.
	To build and install a command, use 'go install' with a version,
	like 'go install example.com/cmd@latest'
	For more information, see https://golang.org/doc/go-get-install-deprecation
	or run 'go help get' or 'go help install'.
bari@ubuntu24:~/YaQQrQ/workspace$ go install github.com/aktau/github-release@latest
go: downloading github.com/aktau/github-release v0.10.1
go: finding module for package github.com/voxelbrain/goptions
go: finding module for package github.com/github-release/github-release/github
go: finding module for package github.com/dustin/go-humanize
go: downloading github.com/dustin/go-humanize v1.0.1
go: downloading github.com/voxelbrain/goptions v0.0.0-20180630082107-58cddc247ea2
go: downloading github.com/github-release/github-release v0.10.1
go: found github.com/dustin/go-humanize in github.com/dustin/go-humanize v1.0.1
go: found github.com/github-release/github-release/github in github.com/github-release/github-release v0.10.1
go: found github.com/voxelbrain/goptions in github.com/voxelbrain/goptions v0.0.0-20180630082107-58cddc247ea2
go: finding module for package github.com/tomnomnom/linkheader
go: finding module for package github.com/kevinburke/rest/restclient
go: downloading github.com/kevinburke/rest v0.0.0-20240617045629-3ed0ad3487f0
go: downloading github.com/tomnomnom/linkheader v0.0.0-20180905144013-02ca5825eb80
go: found github.com/kevinburke/rest/restclient in github.com/kevinburke/rest v0.0.0-20240617045629-3ed0ad3487f0
go: found github.com/tomnomnom/linkheader in github.com/tomnomnom/linkheader v0.0.0-20180905144013-02ca5825eb80
bari@ubuntu24:~/YaQQrQ/workspace$ git clone https://github.com/${GITHUB_USERNAME}/lab08 projects/lab09
Cloning into 'projects/lab09'...
remote: Enumerating objects: 104, done.
remote: Counting objects: 100% (104/104), done.
remote: Compressing objects: 100% (58/58), done.
remote: Total 104 (delta 33), reused 102 (delta 31), pack-reused 0 (from 0)
Receiving objects: 100% (104/104), 62.43 KiB | 1.25 MiB/s, done.
Resolving deltas: 100% (33/33), done.
bari@ubuntu24:~/YaQQrQ/workspace$ cd projects/lab09
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab09$ git remote remove origin
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab09$ git remote add origin https://github.com/${GITHUB_USERNAME}/lab09
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab09$ gsed -i 's/lab08/lab09/g' README.md
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab09$ $PACKAGE_MANAGER install ${GPG_PACKAGE_NAME}
Error: Could not open lock file /var/lib/dpkg/lock-frontend - open (13: Permission denied)
Error: Unable to acquire the dpkg frontend lock (/var/lib/dpkg/lock-frontend), are you root?
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab09$ sudo $PACKAGE_MANAGER install ${GPG_PACKAGE_NAME}
gpg is already the newest version (2.4.4-2ubuntu23).
gpg set to manually installed.
Summary:                    
  Upgrading: 0, Installing: 0, Removing: 0, Not Upgrading: 3
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab09$ gpg --list-secret-keys --keyid-format LONG
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab09$ gpg --full-generate-key
gpg (GnuPG) 2.4.4; Copyright (C) 2024 g10 Code GmbH
This is free software: you are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.

Please select what kind of key you want:
   (1) RSA and RSA
   (2) DSA and Elgamal
   (3) DSA (sign only)
   (4) RSA (sign only)
   (9) ECC (sign and encrypt) *default*
  (10) ECC (sign only)
  (14) Existing key from card
Your selection? 1
RSA keys may be between 1024 and 4096 bits long.
What keysize do you want? (3072) 4096
Requested keysize is 4096 bits
Please specify how long the key should be valid.
         0 = key does not expire
      <n>  = key expires in n days
      <n>w = key expires in n weeks
      <n>m = key expires in n months
      <n>y = key expires in n years
Key is valid for? (0) 0
Key does not expire at all
Is this correct? (y/N) y

GnuPG needs to construct a user ID to identify your key.

Real name: Bari
Email address: bari.tsapaev@gmail.com
Comment: i
You selected this USER-ID:
    "Bari (i) <bari.tsapaev@gmail.com>"

Change (N)ame, (C)omment, (E)mail or (O)kay/(Q)uit? O
We need to generate a lot of random bytes. It is a good idea to perform
some other action (type on the keyboard, move the mouse, utilize the
disks) during the prime generation; this gives the random number
generator a better chance to gain enough entropy.
We need to generate a lot of random bytes. It is a good idea to perform
some other action (type on the keyboard, move the mouse, utilize the
disks) during the prime generation; this gives the random number
generator a better chance to gain enough entropy.
gpg: directory '/home/bari/.gnupg/openpgp-revocs.d' created
gpg: revocation certificate stored as '/home/bari/.gnupg/openpgp-revocs.d/152549A9B210A8D348BD917BC8D2B4EE367A66B7.rev'
public and secret key created and signed.

pub   rsa4096 2025-04-30 [SC]
      152549A9B210A8D348BD917BC8D2B4EE367A66B7
uid                      Bari (i) <bari.tsapaev@gmail.com>
sub   rsa4096 2025-04-30 [E]

bari@ubuntu24:~/YaQQrQ/workspace/projects/lab09$ gpg --list-secret-keys --keyid-format LONG
gpg: checking the trustdb
gpg: marginals needed: 3  completes needed: 1  trust model: pgp
gpg: depth: 0  valid:   1  signed:   0  trust: 0-, 0q, 0n, 0m, 0f, 1u
/home/bari/.gnupg/pubring.kbx
-----------------------------
sec   rsa4096/C8D2B4EE367A66B7 2025-04-30 [SC]
      152549A9B210A8D348BD917BC8D2B4EE367A66B7
uid                 [ultimate] Bari (i) <bari.tsapaev@gmail.com>
ssb   rsa4096/33464527A2ADDC40 2025-04-30 [E]

bari@ubuntu24:~/YaQQrQ/workspace/projects/lab09$ gpg -K ${GITHUB_USERNAME}
gpg: error reading key: No secret key
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab09$ GPG_KEY_ID=$(gpg --list-secret-keys --keyid-format LONG | grep ssb | tail -1 | awk '{print $2}' | awk -F'/' '{print $2}')
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab09$ GPG_SEC_KEY_ID=$(gpg --list-secret-keys --keyid-format LONG | grep sec | tail -1 | awk '{print $2}' | awk -F'/' '{print $2}')
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab09$ gpg --armor --export ${GPG_KEY_ID} | pbcopy
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab09$ pbpaste
pbpastebari@ubuntu24:~/YaQQrQ/workspace/projects/open https://github.com/settings/keysgs/keys
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab09$ Gtk-Message: 19:41:38.178: Not loading module "atk-bridge": The functionality is provided by GTK natively. Please try to not load it.

bari@ubuntu24:~/YaQQrQ/workspace/projects/lab09$ git config user.signingkey ${GPG_SEC_KEY_ID}
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab09$ git config gpg.program gpg
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab09$ test -r ~/.bash_profile && echo 'export GPG_TTY=$(tty)' >> ~/.bash_profile
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab09$ echo 'export GPG_TTY=$(tty)' >> ~/.profile
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab09$ cmake -H. -B_build -DCPACK_GENERATOR="TGZ"
-- [hunter] Initializing Hunter workspace (26c79d587883ec910bce168e25f6ac4595f97033)
-- [hunter]   https://github.com/cpp-pm/hunter/archive/v0.25.8.tar.gz
-- [hunter]   -> /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5
CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/Hunter:34 (include)
  cmake/HunterGate.cmake:540 (include)
  CMakeLists.txt:4 (HunterGate)


CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_calculate_config_sha1.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:8 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/Hunter:34 (include)
  cmake/HunterGate.cmake:540 (include)
  CMakeLists.txt:4 (HunterGate)


CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_calculate_config_sha1.cmake:9 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:8 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/Hunter:34 (include)
  cmake/HunterGate.cmake:540 (include)
  CMakeLists.txt:4 (HunterGate)


CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_make_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_calculate_config_sha1.cmake:10 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:8 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/Hunter:34 (include)
  cmake/HunterGate.cmake:540 (include)
  CMakeLists.txt:4 (HunterGate)


CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_make_directory.cmake:7 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_calculate_config_sha1.cmake:10 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:8 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/Hunter:34 (include)
  cmake/HunterGate.cmake:540 (include)
  CMakeLists.txt:4 (HunterGate)


CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_calculate_self.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:9 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/Hunter:34 (include)
  cmake/HunterGate.cmake:540 (include)
  CMakeLists.txt:4 (HunterGate)


CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_calculate_toolchain_sha1.cmake:5 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:10 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/Hunter:34 (include)
  cmake/HunterGate.cmake:540 (include)
  CMakeLists.txt:4 (HunterGate)


CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_make_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_calculate_toolchain_sha1.cmake:6 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:10 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/Hunter:34 (include)
  cmake/HunterGate.cmake:540 (include)
  CMakeLists.txt:4 (HunterGate)


CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_make_directory.cmake:7 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_calculate_toolchain_sha1.cmake:6 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:10 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/Hunter:34 (include)
  cmake/HunterGate.cmake:540 (include)
  CMakeLists.txt:4 (HunterGate)


CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_set_config_location.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:13 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/Hunter:34 (include)
  cmake/HunterGate.cmake:540 (include)
  CMakeLists.txt:4 (HunterGate)


CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_calculate_self.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_finalize.cmake:6 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/Hunter:34 (include)
  cmake/HunterGate.cmake:540 (include)
  CMakeLists.txt:4 (HunterGate)


CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_private_data.cmake:12 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/Hunter:35 (include)
  cmake/HunterGate.cmake:540 (include)
  CMakeLists.txt:4 (HunterGate)


CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_calculate_self.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_initialize.cmake:4 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/Hunter:36 (include)
  cmake/HunterGate.cmake:540 (include)
  CMakeLists.txt:4 (HunterGate)


-- The C compiler identification is GNU 14.2.0
-- The CXX compiler identification is GNU 14.2.0
-- Detecting C compiler ABI info
-- Detecting C compiler ABI info - done
-- Check for working C compiler: /usr/bin/cc - skipped
-- Detecting C compile features
-- Detecting C compile features - done
-- Detecting CXX compiler ABI info
-- Detecting CXX compiler ABI info - done
-- Check for working CXX compiler: /usr/bin/c++ - skipped
-- Detecting CXX compile features
-- Detecting CXX compile features - done
-- [hunter] Calculating Toolchain-SHA1
CMake Deprecation Warning at CMakeLists.txt:1 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.


-- [hunter] Calculating Config-SHA1
-- [hunter] HUNTER_ROOT: /home/bari/.hunter
-- [hunter] [ Hunter-ID: 26c79d5 | Toolchain-ID: 51730f9 | Config-ID: 37d6cfd ]
CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_load_from_cache.cmake:4 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:21 (hunter_add_package)


CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_calculate_config_sha1.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:8 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_load_from_cache.cmake:4 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:21 (hunter_add_package)


CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_calculate_config_sha1.cmake:9 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:8 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_load_from_cache.cmake:4 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:21 (hunter_add_package)


CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_make_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_calculate_config_sha1.cmake:10 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:8 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_load_from_cache.cmake:4 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:21 (hunter_add_package)


CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_make_directory.cmake:7 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_calculate_config_sha1.cmake:10 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:8 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_load_from_cache.cmake:4 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:21 (hunter_add_package)


CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_calculate_self.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:9 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_load_from_cache.cmake:4 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:21 (hunter_add_package)


CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_calculate_toolchain_sha1.cmake:5 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:10 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_load_from_cache.cmake:4 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:21 (hunter_add_package)


CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_make_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_calculate_toolchain_sha1.cmake:6 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:10 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_load_from_cache.cmake:4 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:21 (hunter_add_package)


CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_make_directory.cmake:7 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_calculate_toolchain_sha1.cmake:6 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:10 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_load_from_cache.cmake:4 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:21 (hunter_add_package)


CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_set_config_location.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:13 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_load_from_cache.cmake:4 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:21 (hunter_add_package)


CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_calculate_self.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_finalize.cmake:6 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_load_from_cache.cmake:4 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:21 (hunter_add_package)


CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_cache_run.cmake:6 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_load_from_cache.cmake:5 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:21 (hunter_add_package)


CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_calculate_config_sha1.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:8 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_cache_run.cmake:6 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_load_from_cache.cmake:5 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:21 (hunter_add_package)


CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_calculate_config_sha1.cmake:9 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:8 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_cache_run.cmake:6 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_load_from_cache.cmake:5 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:21 (hunter_add_package)


CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_make_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_calculate_config_sha1.cmake:10 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:8 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_cache_run.cmake:6 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_load_from_cache.cmake:5 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:21 (hunter_add_package)


CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_make_directory.cmake:7 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_calculate_config_sha1.cmake:10 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:8 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_cache_run.cmake:6 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_load_from_cache.cmake:5 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:21 (hunter_add_package)


CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_calculate_self.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:9 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_cache_run.cmake:6 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_load_from_cache.cmake:5 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:21 (hunter_add_package)


CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_calculate_toolchain_sha1.cmake:5 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:10 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_cache_run.cmake:6 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_load_from_cache.cmake:5 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:21 (hunter_add_package)


CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_make_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_calculate_toolchain_sha1.cmake:6 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:10 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_cache_run.cmake:6 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_load_from_cache.cmake:5 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:21 (hunter_add_package)


CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_make_directory.cmake:7 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_calculate_toolchain_sha1.cmake:6 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:10 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_cache_run.cmake:6 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_load_from_cache.cmake:5 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:21 (hunter_add_package)


CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_set_config_location.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:13 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_cache_run.cmake:6 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_load_from_cache.cmake:5 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:21 (hunter_add_package)


CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_calculate_self.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_finalize.cmake:6 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_cache_run.cmake:6 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_load_from_cache.cmake:5 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:21 (hunter_add_package)


CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_make_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_create_cache_meta_directory.cmake:5 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_load_from_cache.cmake:6 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:21 (hunter_add_package)


CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_make_directory.cmake:7 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_create_cache_meta_directory.cmake:5 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_load_from_cache.cmake:6 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:21 (hunter_add_package)


CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_make_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_create_cache_meta_directory.cmake:5 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_save_to_cache.cmake:4 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_download.cmake:26 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:21 (hunter_add_package)


CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_make_directory.cmake:7 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_create_cache_meta_directory.cmake:5 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_save_to_cache.cmake:4 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_download.cmake:26 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:21 (hunter_add_package)


CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_save_to_cache.cmake:7 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_download.cmake:26 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:21 (hunter_add_package)


CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_make_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_save_to_cache.cmake:8 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_download.cmake:26 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:21 (hunter_add_package)


CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_make_directory.cmake:7 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_save_to_cache.cmake:8 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_download.cmake:26 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:21 (hunter_add_package)


-- [hunter] GTEST_ROOT: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Install (ver.: 1.11.0)
-- [hunter] Building GTest
loading initial cache file /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/cache.cmake
loading initial cache file /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/args.cmake
CMake Deprecation Warning at CMakeLists.txt:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.


-- The C compiler identification is GNU 14.2.0
-- The CXX compiler identification is GNU 14.2.0
-- Check for working C compiler: /usr/bin/cc - skipped
-- Detecting C compile features
-- Detecting C compile features - done
-- Check for working CXX compiler: /usr/bin/c++ - skipped
-- Detecting CXX compile features
-- Detecting CXX compile features - done
-- Configuring done (0.1s)
-- Generating done (0.0s)
-- Build files have been written to: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Build
[  6%] Creating directories for 'GTest-Release'
[ 12%] Performing download step (download, verify and extract) for 'GTest-Release'
-- Downloading...
   dst='/home/bari/.hunter/_Base/Download/GTest/1.11.0/7b100bb/release-1.11.0.tar.gz'
   timeout='none'
   inactivity timeout='none'
-- Using src='https://github.com/google/googletest/archive/release-1.11.0.tar.gz'
-- [download 1% complete]
-- [download 2% complete]
-- [download 4% complete]
-- [download 5% complete]
-- [download 6% complete]
-- [download 7% complete]
-- [download 8% complete]
-- [download 9% complete]
-- [download 11% complete]
-- [download 13% complete]
-- [download 15% complete]
-- [download 16% complete]
-- [download 18% complete]
-- [download 19% complete]
-- [download 20% complete]
-- [download 22% complete]
-- [download 24% complete]
-- [download 25% complete]
-- [download 26% complete]
-- [download 27% complete]
-- [download 28% complete]
-- [download 29% complete]
-- [download 31% complete]
-- [download 33% complete]
-- [download 34% complete]
-- [download 35% complete]
-- [download 36% complete]
-- [download 38% complete]
-- [download 39% complete]
-- [download 41% complete]
-- [download 43% complete]
-- [download 45% complete]
-- [download 46% complete]
-- [download 48% complete]
-- [download 50% complete]
-- [download 51% complete]
-- [download 52% complete]
-- [download 53% complete]
-- [download 54% complete]
-- [download 56% complete]
-- [download 57% complete]
-- [download 58% complete]
-- [download 59% complete]
-- [download 61% complete]
-- [download 63% complete]
-- [download 64% complete]
-- [download 66% complete]
-- [download 67% complete]
-- [download 68% complete]
-- [download 70% complete]
-- [download 71% complete]
-- [download 73% complete]
-- [download 75% complete]
-- [download 76% complete]
-- [download 77% complete]
-- [download 79% complete]
-- [download 80% complete]
-- [download 81% complete]
-- [download 82% complete]
-- [download 83% complete]
-- [download 84% complete]
-- [download 85% complete]
-- [download 86% complete]
-- [download 87% complete]
-- [download 88% complete]
-- [download 89% complete]
-- [download 91% complete]
-- [download 93% complete]
-- [download 95% complete]
-- [download 97% complete]
-- [download 99% complete]
-- [download 100% complete]
-- verifying file...
       file='/home/bari/.hunter/_Base/Download/GTest/1.11.0/7b100bb/release-1.11.0.tar.gz'
-- Downloading... done
-- extracting...
     src='/home/bari/.hunter/_Base/Download/GTest/1.11.0/7b100bb/release-1.11.0.tar.gz'
     dst='/home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Source'
-- extracting... [tar xfz]
-- extracting... [analysis]
-- extracting... [rename]
-- extracting... [clean up]
-- extracting... done
[ 18%] No update step for 'GTest-Release'
[ 25%] No patch step for 'GTest-Release'
[ 31%] Performing configure step for 'GTest-Release'
loading initial cache file /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/cache.cmake
loading initial cache file /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/args.cmake
CMake Deprecation Warning at CMakeLists.txt:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.


-- The C compiler identification is GNU 14.2.0
-- The CXX compiler identification is GNU 14.2.0
-- Check for working C compiler: /usr/bin/cc - skipped
-- Detecting C compile features
-- Detecting C compile features - done
-- Check for working CXX compiler: /usr/bin/c++ - skipped
-- Detecting CXX compile features
-- Detecting CXX compile features - done
CMake Deprecation Warning at googlemock/CMakeLists.txt:45 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.


CMake Deprecation Warning at googletest/CMakeLists.txt:56 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.


-- Found Python: /usr/bin/python3 (found version "3.13.3") found components: Interpreter
-- Performing Test CMAKE_HAVE_LIBC_PTHREAD
-- Performing Test CMAKE_HAVE_LIBC_PTHREAD - Success
-- Found Threads: TRUE
-- Configuring done (0.3s)
-- Generating done (0.0s)
-- Build files have been written to: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Build/GTest-Release-prefix/src/GTest-Release-build
[ 37%] Performing build step for 'GTest-Release'
[ 12%] Building CXX object googletest/CMakeFiles/gtest.dir/src/gtest-all.cc.o
[ 25%] Linking CXX static library ../lib/libgtest.a
[ 25%] Built target gtest
[ 50%] Building CXX object googletest/CMakeFiles/gtest_main.dir/src/gtest_main.cc.o
[ 50%] Building CXX object googlemock/CMakeFiles/gmock.dir/src/gmock-all.cc.o
[ 62%] Linking CXX static library ../lib/libgtest_main.a
[ 62%] Built target gtest_main
[ 75%] Linking CXX static library ../lib/libgmock.a
[ 75%] Built target gmock
[ 87%] Building CXX object googlemock/CMakeFiles/gmock_main.dir/src/gmock_main.cc.o
[100%] Linking CXX static library ../lib/libgmock_main.a
[100%] Built target gmock_main
[ 43%] Performing install step for 'GTest-Release'
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gmock
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gmock/gmock-spec-builders.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gmock/gmock-actions.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gmock/gmock-more-matchers.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gmock/gmock-nice-strict.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gmock/gmock-function-mocker.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gmock/gmock-cardinalities.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gmock/gmock-more-actions.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gmock/internal
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gmock/internal/custom
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gmock/internal/custom/gmock-generated-actions.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gmock/internal/custom/gmock-matchers.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gmock/internal/custom/gmock-port.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gmock/internal/custom/README.md
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gmock/internal/gmock-pp.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gmock/internal/gmock-internal-utils.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gmock/internal/gmock-port.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gmock/gmock-matchers.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gmock/gmock.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/lib/libgmock.a
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/lib/libgmock_main.a
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/lib/pkgconfig/gmock.pc
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/lib/pkgconfig/gmock_main.pc
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/lib/cmake/GTest/GTestTargets.cmake
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/lib/cmake/GTest/GTestTargets-release.cmake
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/lib/cmake/GTest/GTestConfigVersion.cmake
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/lib/cmake/GTest/GTestConfig.cmake
-- Up-to-date: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gtest
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gtest/gtest.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gtest/gtest-printers.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gtest/gtest-typed-test.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gtest/gtest-death-test.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gtest/gtest_prod.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gtest/gtest_pred_impl.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gtest/gtest-matchers.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gtest/gtest-spi.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gtest/internal
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gtest/internal/gtest-port-arch.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gtest/internal/gtest-death-test-internal.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gtest/internal/gtest-filepath.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gtest/internal/gtest-string.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gtest/internal/gtest-internal.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gtest/internal/gtest-type-util.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gtest/internal/gtest-port.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gtest/internal/gtest-param-util.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gtest/internal/custom
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gtest/internal/custom/gtest.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gtest/internal/custom/gtest-printers.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gtest/internal/custom/gtest-port.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gtest/internal/custom/README.md
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gtest/gtest-test-part.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gtest/gtest-param-test.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gtest/gtest-message.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/lib/libgtest.a
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/lib/libgtest_main.a
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/lib/pkgconfig/gtest.pc
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/lib/pkgconfig/gtest_main.pc
loading initial cache file /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/args.cmake
CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/scripts/try-copy-license.cmake:5 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.


[ 50%] Completed 'GTest-Release'
[ 50%] Built target GTest-Release
[ 56%] Creating directories for 'GTest-Debug'
[ 62%] Performing download step (download, verify and extract) for 'GTest-Debug'
-- verifying file...
       file='/home/bari/.hunter/_Base/Download/GTest/1.11.0/7b100bb/release-1.11.0.tar.gz'
-- File already exists and hash match (skip download):
  file='/home/bari/.hunter/_Base/Download/GTest/1.11.0/7b100bb/release-1.11.0.tar.gz'
  SHA1='7b100bb68db8df1060e178c495f3cbe941c9b058'
-- extracting...
     src='/home/bari/.hunter/_Base/Download/GTest/1.11.0/7b100bb/release-1.11.0.tar.gz'
     dst='/home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Source'
-- extracting... [tar xfz]
-- extracting... [analysis]
-- extracting... [rename]
-- extracting... [clean up]
-- extracting... done
[ 68%] No update step for 'GTest-Debug'
[ 75%] No patch step for 'GTest-Debug'
[ 81%] Performing configure step for 'GTest-Debug'
loading initial cache file /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/cache.cmake
loading initial cache file /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/args.cmake
CMake Deprecation Warning at CMakeLists.txt:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.


-- The C compiler identification is GNU 14.2.0
-- The CXX compiler identification is GNU 14.2.0
-- Check for working C compiler: /usr/bin/cc - skipped
-- Detecting C compile features
-- Detecting C compile features - done
-- Check for working CXX compiler: /usr/bin/c++ - skipped
-- Detecting CXX compile features
-- Detecting CXX compile features - done
CMake Deprecation Warning at googlemock/CMakeLists.txt:45 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.


CMake Deprecation Warning at googletest/CMakeLists.txt:56 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.


-- Found Python: /usr/bin/python3 (found version "3.13.3") found components: Interpreter
-- Performing Test CMAKE_HAVE_LIBC_PTHREAD
-- Performing Test CMAKE_HAVE_LIBC_PTHREAD - Success
-- Found Threads: TRUE
-- Configuring done (0.3s)
-- Generating done (0.0s)
-- Build files have been written to: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Build/GTest-Debug-prefix/src/GTest-Debug-build
[ 87%] Performing build step for 'GTest-Debug'
[ 12%] Building CXX object googletest/CMakeFiles/gtest.dir/src/gtest-all.cc.o
[ 25%] Linking CXX static library ../lib/libgtestd.a
[ 25%] Built target gtest
[ 37%] Building CXX object googlemock/CMakeFiles/gmock.dir/src/gmock-all.cc.o
[ 50%] Building CXX object googletest/CMakeFiles/gtest_main.dir/src/gtest_main.cc.o
[ 62%] Linking CXX static library ../lib/libgtest_maind.a
[ 62%] Built target gtest_main
[ 75%] Linking CXX static library ../lib/libgmockd.a
[ 75%] Built target gmock
[ 87%] Building CXX object googlemock/CMakeFiles/gmock_main.dir/src/gmock_main.cc.o
[100%] Linking CXX static library ../lib/libgmock_maind.a
[100%] Built target gmock_main
[ 93%] Performing install step for 'GTest-Debug'
-- Up-to-date: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include
-- Up-to-date: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gmock
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gmock/gmock-spec-builders.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gmock/gmock-actions.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gmock/gmock-more-matchers.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gmock/gmock-nice-strict.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gmock/gmock-function-mocker.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gmock/gmock-cardinalities.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gmock/gmock-more-actions.h
-- Up-to-date: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gmock/internal
-- Up-to-date: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gmock/internal/custom
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gmock/internal/custom/gmock-generated-actions.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gmock/internal/custom/gmock-matchers.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gmock/internal/custom/gmock-port.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gmock/internal/custom/README.md
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gmock/internal/gmock-pp.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gmock/internal/gmock-internal-utils.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gmock/internal/gmock-port.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gmock/gmock-matchers.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gmock/gmock.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/lib/libgmockd.a
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/lib/libgmock_maind.a
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/lib/pkgconfig/gmock.pc
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/lib/pkgconfig/gmock_main.pc
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/lib/cmake/GTest/GTestTargets.cmake
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/lib/cmake/GTest/GTestTargets-debug.cmake
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/lib/cmake/GTest/GTestConfigVersion.cmake
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/lib/cmake/GTest/GTestConfig.cmake
-- Up-to-date: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include
-- Up-to-date: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gtest
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gtest/gtest.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gtest/gtest-printers.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gtest/gtest-typed-test.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gtest/gtest-death-test.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gtest/gtest_prod.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gtest/gtest_pred_impl.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gtest/gtest-matchers.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gtest/gtest-spi.h
-- Up-to-date: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gtest/internal
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gtest/internal/gtest-port-arch.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gtest/internal/gtest-death-test-internal.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gtest/internal/gtest-filepath.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gtest/internal/gtest-string.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gtest/internal/gtest-internal.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gtest/internal/gtest-type-util.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gtest/internal/gtest-port.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gtest/internal/gtest-param-util.h
-- Up-to-date: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gtest/internal/custom
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gtest/internal/custom/gtest.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gtest/internal/custom/gtest-printers.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gtest/internal/custom/gtest-port.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gtest/internal/custom/README.md
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gtest/gtest-test-part.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gtest/gtest-param-test.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/include/gtest/gtest-message.h
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/lib/libgtestd.a
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/lib/libgtest_maind.a
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/lib/pkgconfig/gtest.pc
-- Installing: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/Install/lib/pkgconfig/gtest_main.pc
loading initial cache file /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest/args.cmake
CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.25.8/26c79d5/Unpacked/scripts/try-copy-license.cmake:5 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.


[100%] Completed 'GTest-Debug'
[100%] Built target GTest-Debug
-- [hunter] Build step successful (dir: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Build/GTest)
-- [hunter] Cache saved: /home/bari/.hunter/_Base/Cache/raw/68cc47c9ea1a8598772859861556ea75cac972bc.tar.bz2
CMake Warning (dev) at CMakeLists.txt:22 (find_package):
  Policy CMP0144 is not set: find_package uses upper-case <PACKAGENAME>_ROOT
  variables.  Run "cmake --help-policy CMP0144" for policy details.  Use the
  cmake_policy command to set the policy and suppress this warning.

  CMake variable GTEST_ROOT is set to:

    /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Install

  Environment variable GTEST_ROOT is set to:

    /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Install

  For compatibility, find_package is ignoring the variable, but code in a
  .cmake module might still use it.
This warning is for project developers.  Use -Wno-dev to suppress it.

-- Found GTest: /home/bari/.hunter/_Base/26c79d5/51730f9/37d6cfd/Install/lib/cmake/GTest/GTestConfig.cmake (found version "1.11.0")
-- Configuring done (21.1s)
-- Generating done (0.0s)
CMake Warning:
  Manually-specified variables were not used by the project:

    CPACK_GENERATOR


-- Build files have been written to: /home/bari/YaQQrQ/workspace/projects/lab09/_build
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab09$ cmake --build _build --target package
gmake: *** No rule to make target 'package'.  Stop.
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab09$ cmake --build _build --target package
gmake: *** No rule to make target 'package'.  Stop.
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab09$ sudo cmake --build _build --target package
gmake: *** No rule to make target 'package'.  Stop.
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab09$ git tag -s v0.1.0.0
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab09$ git tag -v v0.1.0.0
object 51ccb6339e3a377db46a51915431d4d32c9c7e41
type commit
tag v0.1.0.0
tagger YaQQrQ <bari.tsapaev@gmail.com> 1746042577 +0000

tag 0.1.0.0
gpg: Signature made Ср 30 апр 2025 19:50:14 UTC
gpg:                using RSA key 152549A9B210A8D348BD917BC8D2B4EE367A66B7
gpg: Good signature from "Bari (i) <bari.tsapaev@gmail.com>" [ultimate]
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab09$ git show v0.1.0.0
tag v0.1.0.0
Tagger: YaQQrQ <bari.tsapaev@gmail.com>
Date:   Wed Apr 30 19:49:37 2025 +0000

tag 0.1.0.0
-----BEGIN PGP SIGNATURE-----

iQIzBAABCgAdFiEEFSVJqbIQqNNIvZF7yNK07jZ6ZrcFAmgSfvYACgkQyNK07jZ6
ZreaPxAAjhB9O72HpiTe3AHwr0mUInmUwYC9Vm4kkF17O5brJ1oqaWM5GrDh8a4H
yFbJQxdm+tV0E2lAgj2G8dw9Cr84v8pe0q1nIK3/tKQtGmQDltDP9o2v1SIzlAkP
W8bde893YBB+OK7a5NhHQWI1uSQpEKilOok1FVBcHRbW3MH0KcZVA9qXXcCnCD4Y
I/NjL8VcVhnI0OkEV1kFr2p5FgFgJuA25Ldw6MRO3xPiKDQ7ywN4gA+mUpBleLwB
ystEwiw7NDTQ/ADKo+It1p+KYAalC1D4vUKoEb8+qhkBq7BdqFhxBS205U9ZnMkE
uVYO6chwOx9kHC8erYKwLm8wUmcsOhn/J0ULJU4HdAZwXLlC1I0Pf4lWGz2a9kKT
H/bMO8vp0oBpazBpjzlsC20cqFHoCIOTsf0EeyKoLLs4K9rwGRGf2YKouhWZuQ7K
7hM4wEDrjS1hi/1+krCCJip/b1oydjGuzbXAwq4VjXRW3qilky1fUwFbCIs1fzoH
s/z/+bbeHuOcgFQtTapaHHjpSsEvyGin7l8EiGWtKNfsYangLiaYESJWWOFhrvdq
lJ3Hextqos0fmpEuwQvbnueBtf3QzjV+CRtPqj4XQ8c4m+/A6QA0ynfz2SOlst7M
Ew1Pg2ateI3N3fieJYjmQ2ixddu6WGK7FQXIPdi35CVBelHUpKE=
=x1m/
-----END PGP SIGNATURE-----

commit 51ccb6339e3a377db46a51915431d4d32c9c7e41 (HEAD -> master, tag: v0.1.0.0)
Author: YaQQrQ <bari.tsapaev@gmail.com>
Date:   Wed Apr 30 19:24:31 2025 +0000

    readme

diff --git a/.travis.yml.swn b/.travis.yml.swn
new file mode 100644
index 0000000..f53a840
Binary files /dev/null and b/.travis.yml.swn differ
diff --git a/.travis.yml.swo b/.travis.yml.swo
new file mode 100644
index 0000000..a7bfac2
Binary files /dev/null and b/.travis.yml.swo differ
diff --git a/CMakeLists.txt b/CMakeLists.txt
index 1855c5e..36a1d95 100644
--- a/CMakeLists.txt
+++ b/CMakeLists.txt
@@ -2,8 +2,8 @@ cmake_minimum_required(VERSION 3.14)
 
 include("cmake/HunterGate.cmake")
 HunterGate(
-    URL "https://github.com/cpp-pm/hunter/archive/v0.23.314.tar.gz"
-    SHA1 "572541b3a9e2c1ccb0c0e552f6dc12219c0d6a0b"
+    URL "https://github.com/cpp-pm/hunter/archive/v0.25.8.tar.gz"
+    SHA1 "26c79d587883ec910bce168e25f6ac4595f97033"
     LOCAL
 )
 
diff --git a/README.md b/README.md
index b4c7603..5f4dcf9 100644
--- a/README.md
+++ b/README.md
@@ -1,3088 +1,587 @@
 bari@ubuntu24:~$ export GITHUB_USERNAME=YaQQrQ
-bari@ubuntu24:~$ alias gsed=sed
 bari@ubuntu24:~$ cd ${GITHUB_USERNAME}/workspace
 bari@ubuntu24:~/YaQQrQ/workspace$ pushd .
 ~/YaQQrQ/workspace ~/YaQQrQ/workspace
 bari@ubuntu24:~/YaQQrQ/workspace$ source scripts/activate
-bari@ubuntu24:~/YaQQrQ/workspace$ git clone https://github.com/${GITHUB_USERNAME}/lab06 projects/lab07
-Cloning into 'projects/lab07'...
-remote: Enumerating objects: 257, done.
-remote: Counting objects: 100% (257/257), done.
-remote: Compressing objects: 100% (142/142), done.
-remote: Total 257 (delta 88), reused 250 (delta 84), pack-reused 0 (from 0)
-Receiving objects: 100% (257/257), 1.05 MiB | 1.80 MiB/s, done.
-Resolving deltas: 100% (88/88), done.
-bari@ubuntu24:~/YaQQrQ/workspace$ cd projects/lab07
-bari@ubuntu24:~/YaQQrQ/workspace/projects/lab07$ git remote remove origin
-bari@ubuntu24:~/YaQQrQ/workspace/projects/lab07$ git remote add origin https://github.com/${GITHUB_USERNAME}/lab07
-bari@ubuntu24:~/YaQQrQ/workspace/projects/lab07$ mkdir -p cmake
-bari@ubuntu24:~/YaQQrQ/workspace/projects/lab07$ wget https://raw.githubusercontent.com/cpp-pm/gate/master/cmake/HunterGate.cmake -O cmake/HunterGate.cmake
---2025-04-29 14:31:40--  https://raw.githubusercontent.com/cpp-pm/gate/master/cmake/HunterGate.cmake
-Resolving raw.githubusercontent.com (raw.githubusercontent.com)... 185.199.110.133, 185.199.108.133, 185.199.109.133, ...
-Connecting to raw.githubusercontent.com (raw.githubusercontent.com)|185.199.110.133|:443... connected.
-HTTP request sent, awaiting response... 200 OK
-Length: 17231 (17K) [text/plain]
-Saving to: ‘cmake/HunterGate.cmake’
-
-cmake/HunterGate.cmake    100%[====================================>]  16,83K  --.-KB/s    in 0,002s  
-
-2025-04-29 14:31:40 (7,51 MB/s) - ‘cmake/HunterGate.cmake’ saved [17231/17231]
-
-bari@ubuntu24:~/YaQQrQ/workspace/projects/lab07$ gsed -i '/cmake_minimum_required(VERSION 3.4)/a\
-> include("cmake/HunterGate.cmake")
-HunterGate(
-    URL "https://github.com/cpp-pm/hunter/archive/v0.23.251.tar.gz"
-    SHA1 "5659b15dc0884d4b03dbd95710e6a1fa0fc3258d"
-)
-> ' CMakeLists.txt
-sed: -e expression #1, char 76: extra characters after command
-bari@ubuntu24:~/YaQQrQ/workspace/projects/lab07$ ^C
-bari@ubuntu24:~/YaQQrQ/workspace/projects/lab07$ gsed -i '/cmake_minimum_required(VERSION 3.4)/a \
-> include("cmake/HunterGate.cmake") \
-> HunterGate( \
-> URL "https://github.com/cpp-pm/hunter/archive/v0.23.251.tar.gz" \
-> SHA1 "5659b15dc0884d4b03dbd95710e6a1fa0fc3258d" \
-> )' CMakeLists.txt
-bari@ubuntu24:~/YaQQrQ/workspace/projects/lab07$ git rm -rf third-party/gtest
-rm 'third-party/gtest'
-bari@ubuntu24:~/YaQQrQ/workspace/projects/lab07$ gsed -i '/set(PRINT_VERSION_STRING "v\${PRINT_VERSION}")/a\
+bari@ubuntu24:~/YaQQrQ/workspace$ git clone https://github.com/${GITHUB_USERNAME}/lab07 lab08
+Cloning into 'lab08'...
+remote: Enumerating objects: 92, done.
+remote: Counting objects: 100% (92/92), done.
+remote: Compressing objects: 100% (53/53), done.
+remote: Total 92 (delta 28), reused 89 (delta 26), pack-reused 0 (from 0)
+Receiving objects: 100% (92/92), 54.63 KiB | 165.00 KiB/s, done.
+Resolving deltas: 100% (28/28), done.
+bari@ubuntu24:~/YaQQrQ/workspace$ cd lab08
+bari@ubuntu24:~/YaQQrQ/workspace/lab08$ git submodule update --init
+bari@ubuntu24:~/YaQQrQ/workspace/lab08$ git remote remove origin
+bari@ubuntu24:~/YaQQrQ/workspace/lab08$ git remote add origin https://github.com/${GITHUB_USERNAME}/lab08
+bari@ubuntu24:~/YaQQrQ/workspace/lab08$ cat > Dockerfile <<EOF
+> FROM ubuntu:18.04
+> EOF
+bari@ubuntu24:~/YaQQrQ/workspace/lab08$ cat >> Dockerfile <<EOF
 > 
-> hunter_add_package(GTest)
-> find_package(GTest CONFIG REQUIRED)
-> ' CMakeLists.txt
-sed: -e expression #1, char 54: extra characters after command
-bari@ubuntu24:~/YaQQrQ/workspace/projects/lab07$ gsed -i '/set(PRINT_VERSION_STRING "v\${PRINT_VERSION}")/a \
-> hunter_add_package(GTest) \
-> find_package(GTest CONFIG REQUIRED) \
-> ' CMakeLists.txt
-bari@ubuntu24:~/YaQQrQ/workspace/projects/lab07$ gsed -i 's/add_subdirectory(third-party/gtest)//' CMakeLists.txt
-sed: -e expression #1, char 39: unknown option to `s'
-bari@ubuntu24:~/YaQQrQ/workspace/projects/lab07$ gsed -i 's/add_subdirectory(third-party\/gtest)//' CMakeLists.txt
-bari@ubuntu24:~/YaQQrQ/workspace/projects/lab07$ gsed -i 's/gtest_main/GTest::main/' CMakeLists.txt
-bari@ubuntu24:~/YaQQrQ/workspace/projects/lab07$ cmake -H. -B_builds -DBUILD_TESTS=ON
-CMake Deprecation Warning at CMakeLists.txt:1 (cmake_minimum_required):
-  Compatibility with CMake < 3.5 will be removed from a future version of
-  CMake.
-
-  Update the VERSION argument <min> value or use a ...<max> suffix to tell
-  CMake that the project does not need compatibility with older versions.
-
-
-CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:4 (cmake_minimum_required):
-  Compatibility with CMake < 3.5 will be removed from a future version of
-  CMake.
-
-  Update the VERSION argument <min> value or use a ...<max> suffix to tell
-  CMake that the project does not need compatibility with older versions.
-Call Stack (most recent call first):
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/Hunter:34 (include)
-  cmake/HunterGate.cmake:540 (include)
-  CMakeLists.txt:4 (HunterGate)
-
-
-CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_config_sha1.cmake:4 (cmake_minimum_required):
-  Compatibility with CMake < 3.5 will be removed from a future version of
-  CMake.
-
-  Update the VERSION argument <min> value or use a ...<max> suffix to tell
-  CMake that the project does not need compatibility with older versions.
-Call Stack (most recent call first):
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:8 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/Hunter:34 (include)
-  cmake/HunterGate.cmake:540 (include)
-  CMakeLists.txt:4 (HunterGate)
-
-
-CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
-  Compatibility with CMake < 3.5 will be removed from a future version of
-  CMake.
-
-  Update the VERSION argument <min> value or use a ...<max> suffix to tell
-  CMake that the project does not need compatibility with older versions.
-Call Stack (most recent call first):
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_config_sha1.cmake:9 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:8 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/Hunter:34 (include)
-  cmake/HunterGate.cmake:540 (include)
-  CMakeLists.txt:4 (HunterGate)
-
-
-CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_make_directory.cmake:4 (cmake_minimum_required):
-  Compatibility with CMake < 3.5 will be removed from a future version of
-  CMake.
-
-  Update the VERSION argument <min> value or use a ...<max> suffix to tell
-  CMake that the project does not need compatibility with older versions.
-Call Stack (most recent call first):
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_config_sha1.cmake:10 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:8 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/Hunter:34 (include)
-  cmake/HunterGate.cmake:540 (include)
-  CMakeLists.txt:4 (HunterGate)
-
-
-CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
-  Compatibility with CMake < 3.5 will be removed from a future version of
-  CMake.
-
-  Update the VERSION argument <min> value or use a ...<max> suffix to tell
-  CMake that the project does not need compatibility with older versions.
-Call Stack (most recent call first):
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_make_directory.cmake:7 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_config_sha1.cmake:10 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:8 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/Hunter:34 (include)
-  cmake/HunterGate.cmake:540 (include)
-  CMakeLists.txt:4 (HunterGate)
-
-
-CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_self.cmake:4 (cmake_minimum_required):
-  Compatibility with CMake < 3.5 will be removed from a future version of
-  CMake.
-
-  Update the VERSION argument <min> value or use a ...<max> suffix to tell
-  CMake that the project does not need compatibility with older versions.
-Call Stack (most recent call first):
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:9 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/Hunter:34 (include)
-  cmake/HunterGate.cmake:540 (include)
-  CMakeLists.txt:4 (HunterGate)
-
-
-CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
-  Compatibility with CMake < 3.5 will be removed from a future version of
-  CMake.
-
-  Update the VERSION argument <min> value or use a ...<max> suffix to tell
-  CMake that the project does not need compatibility with older versions.
-Call Stack (most recent call first):
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_toolchain_sha1.cmake:5 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:10 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/Hunter:34 (include)
-  cmake/HunterGate.cmake:540 (include)
-  CMakeLists.txt:4 (HunterGate)
-
-
-CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_make_directory.cmake:4 (cmake_minimum_required):
-  Compatibility with CMake < 3.5 will be removed from a future version of
-  CMake.
-
-  Update the VERSION argument <min> value or use a ...<max> suffix to tell
-  CMake that the project does not need compatibility with older versions.
-Call Stack (most recent call first):
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_toolchain_sha1.cmake:6 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:10 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/Hunter:34 (include)
-  cmake/HunterGate.cmake:540 (include)
-  CMakeLists.txt:4 (HunterGate)
-
-
-CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
-  Compatibility with CMake < 3.5 will be removed from a future version of
-  CMake.
-
-  Update the VERSION argument <min> value or use a ...<max> suffix to tell
-  CMake that the project does not need compatibility with older versions.
-Call Stack (most recent call first):
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_make_directory.cmake:7 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_toolchain_sha1.cmake:6 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:10 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/Hunter:34 (include)
-  cmake/HunterGate.cmake:540 (include)
-  CMakeLists.txt:4 (HunterGate)
-
-
-CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_set_config_location.cmake:4 (cmake_minimum_required):
-  Compatibility with CMake < 3.5 will be removed from a future version of
-  CMake.
-
-  Update the VERSION argument <min> value or use a ...<max> suffix to tell
-  CMake that the project does not need compatibility with older versions.
-Call Stack (most recent call first):
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:13 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/Hunter:34 (include)
-  cmake/HunterGate.cmake:540 (include)
-  CMakeLists.txt:4 (HunterGate)
-
-
-CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_self.cmake:4 (cmake_minimum_required):
-  Compatibility with CMake < 3.5 will be removed from a future version of
-  CMake.
-
-  Update the VERSION argument <min> value or use a ...<max> suffix to tell
-  CMake that the project does not need compatibility with older versions.
-Call Stack (most recent call first):
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:6 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/Hunter:34 (include)
-  cmake/HunterGate.cmake:540 (include)
-  CMakeLists.txt:4 (HunterGate)
-
-
-CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
-  Compatibility with CMake < 3.5 will be removed from a future version of
-  CMake.
-
-  Update the VERSION argument <min> value or use a ...<max> suffix to tell
-  CMake that the project does not need compatibility with older versions.
-Call Stack (most recent call first):
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_private_data.cmake:12 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/Hunter:35 (include)
-  cmake/HunterGate.cmake:540 (include)
-  CMakeLists.txt:4 (HunterGate)
-
-
-CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_self.cmake:4 (cmake_minimum_required):
-  Compatibility with CMake < 3.5 will be removed from a future version of
-  CMake.
-
-  Update the VERSION argument <min> value or use a ...<max> suffix to tell
-  CMake that the project does not need compatibility with older versions.
-Call Stack (most recent call first):
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_initialize.cmake:4 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/Hunter:36 (include)
-  cmake/HunterGate.cmake:540 (include)
-  CMakeLists.txt:4 (HunterGate)
-
-
--- The C compiler identification is GNU 13.3.0
--- The CXX compiler identification is GNU 13.3.0
--- Detecting C compiler ABI info
--- Detecting C compiler ABI info - done
--- Check for working C compiler: /usr/bin/cc - skipped
--- Detecting C compile features
--- Detecting C compile features - done
--- Detecting CXX compiler ABI info
--- Detecting CXX compiler ABI info - done
--- Check for working CXX compiler: /usr/bin/c++ - skipped
--- Detecting CXX compile features
--- Detecting CXX compile features - done
--- [hunter] Calculating Toolchain-SHA1
-CMake Deprecation Warning at CMakeLists.txt:1 (cmake_minimum_required):
-  Compatibility with CMake < 3.5 will be removed from a future version of
-  CMake.
-
-  Update the VERSION argument <min> value or use a ...<max> suffix to tell
-  CMake that the project does not need compatibility with older versions.
-
-
--- [hunter] Calculating Config-SHA1
--- [hunter] HUNTER_ROOT: /home/bari/.hunter
--- [hunter] [ Hunter-ID: 23f1b5a | Toolchain-ID: fb15dbb | Config-ID: bf2be25 ]
-CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:4 (cmake_minimum_required):
-  Compatibility with CMake < 3.5 will be removed from a future version of
-  CMake.
-
-  Update the VERSION argument <min> value or use a ...<max> suffix to tell
-  CMake that the project does not need compatibility with older versions.
-Call Stack (most recent call first):
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:4 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
-  CMakeLists.txt:24 (hunter_add_package)
-
-
-CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_config_sha1.cmake:4 (cmake_minimum_required):
-  Compatibility with CMake < 3.5 will be removed from a future version of
-  CMake.
-
-  Update the VERSION argument <min> value or use a ...<max> suffix to tell
-  CMake that the project does not need compatibility with older versions.
-Call Stack (most recent call first):
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:8 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:4 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
-  CMakeLists.txt:24 (hunter_add_package)
-
-
-CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
-  Compatibility with CMake < 3.5 will be removed from a future version of
-  CMake.
-
-  Update the VERSION argument <min> value or use a ...<max> suffix to tell
-  CMake that the project does not need compatibility with older versions.
-Call Stack (most recent call first):
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_config_sha1.cmake:9 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:8 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:4 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
-  CMakeLists.txt:24 (hunter_add_package)
-
-
-CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_make_directory.cmake:4 (cmake_minimum_required):
-  Compatibility with CMake < 3.5 will be removed from a future version of
-  CMake.
-
-  Update the VERSION argument <min> value or use a ...<max> suffix to tell
-  CMake that the project does not need compatibility with older versions.
-Call Stack (most recent call first):
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_config_sha1.cmake:10 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:8 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:4 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
-  CMakeLists.txt:24 (hunter_add_package)
-
-
-CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
-  Compatibility with CMake < 3.5 will be removed from a future version of
-  CMake.
-
-  Update the VERSION argument <min> value or use a ...<max> suffix to tell
-  CMake that the project does not need compatibility with older versions.
-Call Stack (most recent call first):
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_make_directory.cmake:7 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_config_sha1.cmake:10 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:8 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:4 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
-  CMakeLists.txt:24 (hunter_add_package)
-
-
-CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_self.cmake:4 (cmake_minimum_required):
-  Compatibility with CMake < 3.5 will be removed from a future version of
-  CMake.
-
-  Update the VERSION argument <min> value or use a ...<max> suffix to tell
-  CMake that the project does not need compatibility with older versions.
-Call Stack (most recent call first):
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:9 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:4 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
-  CMakeLists.txt:24 (hunter_add_package)
-
-
-CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
-  Compatibility with CMake < 3.5 will be removed from a future version of
-  CMake.
-
-  Update the VERSION argument <min> value or use a ...<max> suffix to tell
-  CMake that the project does not need compatibility with older versions.
-Call Stack (most recent call first):
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_toolchain_sha1.cmake:5 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:10 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:4 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
-  CMakeLists.txt:24 (hunter_add_package)
-
-
-CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_make_directory.cmake:4 (cmake_minimum_required):
-  Compatibility with CMake < 3.5 will be removed from a future version of
-  CMake.
-
-  Update the VERSION argument <min> value or use a ...<max> suffix to tell
-  CMake that the project does not need compatibility with older versions.
-Call Stack (most recent call first):
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_toolchain_sha1.cmake:6 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:10 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:4 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
-  CMakeLists.txt:24 (hunter_add_package)
-
-
-CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
-  Compatibility with CMake < 3.5 will be removed from a future version of
-  CMake.
-
-  Update the VERSION argument <min> value or use a ...<max> suffix to tell
-  CMake that the project does not need compatibility with older versions.
-Call Stack (most recent call first):
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_make_directory.cmake:7 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_toolchain_sha1.cmake:6 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:10 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:4 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
-  CMakeLists.txt:24 (hunter_add_package)
-
-
-CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_set_config_location.cmake:4 (cmake_minimum_required):
-  Compatibility with CMake < 3.5 will be removed from a future version of
-  CMake.
-
-  Update the VERSION argument <min> value or use a ...<max> suffix to tell
-  CMake that the project does not need compatibility with older versions.
-Call Stack (most recent call first):
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:13 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:4 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
-  CMakeLists.txt:24 (hunter_add_package)
-
-
-CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_self.cmake:4 (cmake_minimum_required):
-  Compatibility with CMake < 3.5 will be removed from a future version of
-  CMake.
-
-  Update the VERSION argument <min> value or use a ...<max> suffix to tell
-  CMake that the project does not need compatibility with older versions.
-Call Stack (most recent call first):
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:6 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:4 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
-  CMakeLists.txt:24 (hunter_add_package)
-
-
-CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:4 (cmake_minimum_required):
-  Compatibility with CMake < 3.5 will be removed from a future version of
-  CMake.
-
-  Update the VERSION argument <min> value or use a ...<max> suffix to tell
-  CMake that the project does not need compatibility with older versions.
-Call Stack (most recent call first):
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_cache_run.cmake:6 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:5 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
-  CMakeLists.txt:24 (hunter_add_package)
-
-
-CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_config_sha1.cmake:4 (cmake_minimum_required):
-  Compatibility with CMake < 3.5 will be removed from a future version of
-  CMake.
-
-  Update the VERSION argument <min> value or use a ...<max> suffix to tell
-  CMake that the project does not need compatibility with older versions.
-Call Stack (most recent call first):
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:8 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_cache_run.cmake:6 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:5 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
-  CMakeLists.txt:24 (hunter_add_package)
-
-
-CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
-  Compatibility with CMake < 3.5 will be removed from a future version of
-  CMake.
-
-  Update the VERSION argument <min> value or use a ...<max> suffix to tell
-  CMake that the project does not need compatibility with older versions.
-Call Stack (most recent call first):
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_config_sha1.cmake:9 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:8 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_cache_run.cmake:6 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:5 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
-  CMakeLists.txt:24 (hunter_add_package)
-
-
-CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_make_directory.cmake:4 (cmake_minimum_required):
-  Compatibility with CMake < 3.5 will be removed from a future version of
-  CMake.
-
-  Update the VERSION argument <min> value or use a ...<max> suffix to tell
-  CMake that the project does not need compatibility with older versions.
-Call Stack (most recent call first):
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_config_sha1.cmake:10 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:8 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_cache_run.cmake:6 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:5 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
-  CMakeLists.txt:24 (hunter_add_package)
-
-
-CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
-  Compatibility with CMake < 3.5 will be removed from a future version of
-  CMake.
-
-  Update the VERSION argument <min> value or use a ...<max> suffix to tell
-  CMake that the project does not need compatibility with older versions.
-Call Stack (most recent call first):
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_make_directory.cmake:7 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_config_sha1.cmake:10 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:8 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_cache_run.cmake:6 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:5 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
-  CMakeLists.txt:24 (hunter_add_package)
-
-
-CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_self.cmake:4 (cmake_minimum_required):
-  Compatibility with CMake < 3.5 will be removed from a future version of
-  CMake.
-
-  Update the VERSION argument <min> value or use a ...<max> suffix to tell
-  CMake that the project does not need compatibility with older versions.
-Call Stack (most recent call first):
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:9 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_cache_run.cmake:6 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:5 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
-  CMakeLists.txt:24 (hunter_add_package)
-
-
-CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
-  Compatibility with CMake < 3.5 will be removed from a future version of
-  CMake.
-
-  Update the VERSION argument <min> value or use a ...<max> suffix to tell
-  CMake that the project does not need compatibility with older versions.
-Call Stack (most recent call first):
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_toolchain_sha1.cmake:5 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:10 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_cache_run.cmake:6 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:5 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
-  CMakeLists.txt:24 (hunter_add_package)
-
-
-CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_make_directory.cmake:4 (cmake_minimum_required):
-  Compatibility with CMake < 3.5 will be removed from a future version of
-  CMake.
-
-  Update the VERSION argument <min> value or use a ...<max> suffix to tell
-  CMake that the project does not need compatibility with older versions.
-Call Stack (most recent call first):
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_toolchain_sha1.cmake:6 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:10 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_cache_run.cmake:6 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:5 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
-  CMakeLists.txt:24 (hunter_add_package)
-
-
-CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
-  Compatibility with CMake < 3.5 will be removed from a future version of
-  CMake.
-
-  Update the VERSION argument <min> value or use a ...<max> suffix to tell
-  CMake that the project does not need compatibility with older versions.
-Call Stack (most recent call first):
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_make_directory.cmake:7 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_toolchain_sha1.cmake:6 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:10 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_cache_run.cmake:6 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:5 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
-  CMakeLists.txt:24 (hunter_add_package)
-
-
-CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_set_config_location.cmake:4 (cmake_minimum_required):
-  Compatibility with CMake < 3.5 will be removed from a future version of
-  CMake.
-
-  Update the VERSION argument <min> value or use a ...<max> suffix to tell
-  CMake that the project does not need compatibility with older versions.
-Call Stack (most recent call first):
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:13 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_cache_run.cmake:6 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:5 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
-  CMakeLists.txt:24 (hunter_add_package)
-
-
-CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_self.cmake:4 (cmake_minimum_required):
-  Compatibility with CMake < 3.5 will be removed from a future version of
-  CMake.
-
-  Update the VERSION argument <min> value or use a ...<max> suffix to tell
-  CMake that the project does not need compatibility with older versions.
-Call Stack (most recent call first):
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:6 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_cache_run.cmake:6 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:5 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
-  CMakeLists.txt:24 (hunter_add_package)
-
-
-CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_make_directory.cmake:4 (cmake_minimum_required):
-  Compatibility with CMake < 3.5 will be removed from a future version of
-  CMake.
-
-  Update the VERSION argument <min> value or use a ...<max> suffix to tell
-  CMake that the project does not need compatibility with older versions.
-Call Stack (most recent call first):
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_create_cache_meta_directory.cmake:5 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:6 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
-  CMakeLists.txt:24 (hunter_add_package)
-
-
-CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
-  Compatibility with CMake < 3.5 will be removed from a future version of
-  CMake.
-
-  Update the VERSION argument <min> value or use a ...<max> suffix to tell
-  CMake that the project does not need compatibility with older versions.
-Call Stack (most recent call first):
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_make_directory.cmake:7 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_create_cache_meta_directory.cmake:5 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:6 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
-  CMakeLists.txt:24 (hunter_add_package)
-
-
-CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_make_directory.cmake:4 (cmake_minimum_required):
-  Compatibility with CMake < 3.5 will be removed from a future version of
-  CMake.
-
-  Update the VERSION argument <min> value or use a ...<max> suffix to tell
-  CMake that the project does not need compatibility with older versions.
-Call Stack (most recent call first):
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_create_cache_meta_directory.cmake:5 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_save_to_cache.cmake:4 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:26 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
-  CMakeLists.txt:24 (hunter_add_package)
-
-
-CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
-  Compatibility with CMake < 3.5 will be removed from a future version of
-  CMake.
-
-  Update the VERSION argument <min> value or use a ...<max> suffix to tell
-  CMake that the project does not need compatibility with older versions.
-Call Stack (most recent call first):
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_make_directory.cmake:7 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_create_cache_meta_directory.cmake:5 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_save_to_cache.cmake:4 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:26 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
-  CMakeLists.txt:24 (hunter_add_package)
-
-
-CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
-  Compatibility with CMake < 3.5 will be removed from a future version of
-  CMake.
-
-  Update the VERSION argument <min> value or use a ...<max> suffix to tell
-  CMake that the project does not need compatibility with older versions.
-Call Stack (most recent call first):
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_save_to_cache.cmake:7 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:26 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
-  CMakeLists.txt:24 (hunter_add_package)
-
-
-CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_make_directory.cmake:4 (cmake_minimum_required):
-  Compatibility with CMake < 3.5 will be removed from a future version of
-  CMake.
-
-  Update the VERSION argument <min> value or use a ...<max> suffix to tell
-  CMake that the project does not need compatibility with older versions.
-Call Stack (most recent call first):
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_save_to_cache.cmake:8 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:26 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
-  CMakeLists.txt:24 (hunter_add_package)
-
-
-CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
-  Compatibility with CMake < 3.5 will be removed from a future version of
-  CMake.
-
-  Update the VERSION argument <min> value or use a ...<max> suffix to tell
-  CMake that the project does not need compatibility with older versions.
-Call Stack (most recent call first):
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_make_directory.cmake:7 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_save_to_cache.cmake::
 (include)
-  CMakeLists.txt:24 (hunter_add_package)
-
-
-CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
-  Compatibility with CMake < 3.5 will be removed from a future version of
-  CMake.
-
-  Update the VERSION argument <min> value or use a ...<max> suffix to tell
-  CMake that the project does not need compatibility with older versions.
-Call Stack (most recent call first):
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_make_directory.cmake:7 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_save_to_cache.cmake::
 (include)
-  CMakeLists.txt:24 (hunter_add_package)
-
-
-CMake Deprecation Warning at /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
-  Compatibility with CMake < 3.5 will be removed from a future version of
-  CMake.
-
-  Update the VERSION argument <min> value or use a ...<max> suffix to tell
-  CMake that the project does not need compatibility with older versions.
-Call Stack (most recent call first):
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_make_directory.cmake:7 (include)
-  /home/bari/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_save_to_cache.cmake:
tag v0.1.0.0
Tagger: YaQQrQ <bari.tsapaev@gmail.com>
Date:   Wed Apr 30 19:49:37 2025 +0000

tag 0.1.0.0
-----BEGIN PGP SIGNATURE-----

iQIzBAABCgAdFiEEFSVJqbIQqNNIvZF7yNK07jZ6ZrcFAmgSfvYACgkQyNK07jZ6
ZreaPxAAjhB9O72HpiTe3AHwr0mUInmUwYC9Vm4kkF17O5brJ1oqaWM5GrDh8a4H
yFbJQxdm+tV0E2lAgj2G8dw9Cr84v8pe0q1nIK3/tKQtGmQDltDP9o2v1SIzlAkP
W8bde893YBB+OK7a5NhHQWI1uSQpEKilOok1FVBcHRbW3MH0KcZVA9qXXcCnCD4Y
I/NjL8VcVhnI0OkEV1kFr2p5FgFgJuA25Ldw6MRO3xPiKDQ7ywN4gA+mUpBleLwB
ystEwiw7NDTQ/ADKo+It1p+KYAalC1D4vUKoEb8+qhkBq7BdqFhxBS205U9ZnMkE
uVYO6chwOx9kHC8erYKwLm8wUmcsOhn/J0ULJU4HdAZwXLlC1I0Pf4lWGz2a9kKT
H/bMO8vp0oBpazBpjzlsC20cqFHoCIOTsf0EeyKoLLs4K9rwGRGf2YKouhWZuQ7K
7hM4wEDrjS1hi/1+krCCJip/b1oydjGuzbXAwq4VjXRW3qilky1fUwFbCIs1fzoH
s/z/+bbeHuOcgFQtTapaHHjpSsEvyGin7l8EiGWtKNfsYangLiaYESJWWOFhrvdq
lJ3Hextqos0fmpEuwQvbnueBtf3QzjV+CRtPqj4XQ8c4m+/A6QA0ynfz2SOlst7M
Ew1Pg2ateI3N3fieJYjmQ2ixddu6WGK7FQXIPdi35CVBelHUpKE=
=x1m/
-----END PGP SIGNATURE-----

commit 51ccb6339e3a377db46a51915431d4d32c9c7e41 (HEAD -> master, tag: v0.1.0.0)
Author: YaQQrQ <bari.tsapaev@gmail.com>
Date:   Wed Apr 30 19:24:31 2025 +0000

    readme

diff --git a/.travis.yml.swn b/.travis.yml.swn
new file mode 100644
index 0000000..f53a840
Binary files /dev/null and b/.travis.yml.swn differ
diff --git a/.travis.yml.swo b/.travis.yml.swo
new file mode 100644
index 0000000..a7bfac2
Binary files /dev/null and b/.travis.yml.swo differ
diff --git a/CMakeLists.txt b/CMakeLists.txt
index 1855c5e..36a1d95 100644
:
Author: YaQQrQ <bari.tsapaev@gmail.com>
Date:   Wed Apr 30 19:24:31 2025 +0000

    readme

diff --git a/.travis.yml.swn b/.travis.yml.swn
new file mode 100644
index 0000000..f53a840
Binary files /dev/null and b/.travis.yml.swn differ
diff --git a/.travis.yml.swo b/.travis.yml.swo
new file mode 100644
index 0000000..a7bfac2
Binary files /dev/null and b/.travis.yml.swo differ
diff --git a/CMakeLists.txt b/CMakeLists.txt
index 1855c5e..36a1d95 100644
--- a/CMakeLists.txt
+++ b/CMakeLists.txt
@@ -2,8 +2,8 @@ cmake_minimum_required(VERSION 3.14)
 
 include("cmake/HunterGate.cmake")
Finishing logfile... (interrupt to abort)
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab09$ git push origin master --tags
Username for 'https://github.com': YaQQrQ
Password for 'https://YaQQrQ@github.com': 
Enumerating objects: 105, done.
Counting objects: 100% (105/105), done.
Delta compression using up to 8 threads
Compressing objects: 100% (57/57), done.
Writing objects: 100% (105/105), 63.17 KiB | 63.17 MiB/s, done.
Total 105 (delta 33), reused 104 (delta 33), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (33/33), done.
remote: error: GH013: Repository rule violations found for refs/heads/master.
remote: 
remote: - GITHUB PUSH PROTECTION
remote:   —————————————————————————————————————————
remote:     Resolve the following violations before pushing again
remote: 
remote:     - Push cannot contain secrets
remote: 
remote:     
remote:      (?) Learn how to resolve a blocked push
remote:      https://docs.github.com/code-security/secret-scanning/working-with-secret-scanning-and-push-protection/working-with-push-protection-from-the-command-line#resolving-a-blocked-push
remote:     
remote:     
remote:       —— GitHub Personal Access Token ——————————————————————
remote:        locations:
remote:          - commit: 3dbefd07df45839aa845f4053ff6222de4a836ba
remote:            path: README.md:2
remote:     
remote:        (?) To push, remove secret from commit(s) or follow this URL to allow the secret.
remote:        https://github.com/YaQQrQ/lab09/security/secret-scanning/unblock-secret/2wSlryyXkNhYi9VaaPairHPwKzP
remote:     
remote: 
remote: 
remote: error: GH013: Repository rule violations found for refs/tags/v0.1.0.0.
remote: 
remote: - GITHUB PUSH PROTECTION
remote:   —————————————————————————————————————————
remote:     Resolve the following violations before pushing again
remote: 
remote:     - Push cannot contain secrets
remote: 
remote:     
remote:      (?) Learn how to resolve a blocked push
remote:      https://docs.github.com/code-security/secret-scanning/working-with-secret-scanning-and-push-protection/working-with-push-protection-from-the-command-line#resolving-a-blocked-push
remote:     
remote:     
remote:       —— GitHub Personal Access Token ——————————————————————
remote:        locations:
remote:          - commit: 3dbefd07df45839aa845f4053ff6222de4a836ba
remote:            path: README.md:2
remote:     
remote:        (?) To push, remove secret from commit(s) or follow this URL to allow the secret.
remote:        https://github.com/YaQQrQ/lab09/security/secret-scanning/unblock-secret/2wSlryyXkNhYi9VaaPairHPwKzP
remote:     
remote: 
remote: 
To https://github.com/YaQQrQ/lab09
 ! [remote rejected] master -> master (push declined due to repository rule violations)
 ! [remote rejected] v0.1.0.0 -> v0.1.0.0 (push declined due to repository rule violations)
error: failed to push some refs to 'https://github.com/YaQQrQ/lab09'
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab09$ git push origin master --tags
Username for 'https://github.com': YaQQrQ
Password for 'https://YaQQrQ@github.com': 
Enumerating objects: 105, done.
Counting objects: 100% (105/105), done.
Delta compression using up to 8 threads
Compressing objects: 100% (57/57), done.
Writing objects: 100% (105/105), 63.17 KiB | 31.58 MiB/s, done.
Total 105 (delta 33), reused 104 (delta 33), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (33/33), done.
To https://github.com/YaQQrQ/lab09
 * [new branch]      master -> master
 * [new tag]         v0.1.0.0 -> v0.1.0.0
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab09$ github-release --version
github-release: command not found
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab09$ sudo apt install golang
Installing:                     
  golang

Installing dependencies:
  golang-1.24      golang-1.24-go   golang-doc  golang-src   pkgconf
  golang-1.24-doc  golang-1.24-src  golang-go   libpkgconf3  pkgconf-bin

Suggested packages:
  bzr  | brz  mercurial  subversion

Summary:
  Upgrading: 0, Installing: 11, Removing: 0, Not Upgrading: 3
  Download size: 51,5 MB
  Space needed: 259 MB / 17,7 GB available

Continue? [Y/n] Y
Get:1 http://ru.archive.ubuntu.com/ubuntu plucky/main amd64 golang-1.24-doc all 1.24.2-1 [114 kB]
Get:2 http://ru.archive.ubuntu.com/ubuntu plucky/main amd64 golang-1.24-src all 1.24.2-1 [22,0 MB]
Get:3 http://ru.archive.ubuntu.com/ubuntu plucky/main amd64 golang-1.24-go amd64 1.24.2-1 [29,2 MB]
Get:4 http://ru.archive.ubuntu.com/ubuntu plucky/main amd64 golang-1.24 all 1.24.2-1 [5 688 B]                
Get:5 http://ru.archive.ubuntu.com/ubuntu plucky/main amd64 golang-src all 2:1.24~2 [5 136 B]                 
Get:6 http://ru.archive.ubuntu.com/ubuntu plucky/main amd64 golang-go amd64 2:1.24~2 [44,0 kB]                
Get:7 http://ru.archive.ubuntu.com/ubuntu plucky/main amd64 golang-doc all 2:1.24~2 [2 778 B]                 
Get:8 http://ru.archive.ubuntu.com/ubuntu plucky/main amd64 golang amd64 2:1.24~2 [2 724 B]                   
Get:9 http://ru.archive.ubuntu.com/ubuntu plucky/main amd64 libpkgconf3 amd64 1.8.1-4 [32,3 kB]               
Get:10 http://ru.archive.ubuntu.com/ubuntu plucky/main amd64 pkgconf-bin amd64 1.8.1-4 [21,6 kB]              
Get:11 http://ru.archive.ubuntu.com/ubuntu plucky/main amd64 pkgconf amd64 1.8.1-4 [16,8 kB]                  
Fetched 51,5 MB in 15s (3 420 kB/s)                                                                           
Selecting previously unselected package golang-1.24-doc.
(Reading database ... 194208 files and directories currently installed.)
Preparing to unpack .../00-golang-1.24-doc_1.24.2-1_all.deb ...
Unpacking golang-1.24-doc (1.24.2-1) ...
Selecting previously unselected package golang-1.24-src.
Preparing to unpack .../01-golang-1.24-src_1.24.2-1_all.deb ...
Unpacking golang-1.24-src (1.24.2-1) ...
Selecting previously unselected package golang-1.24-go.
Preparing to unpack .../02-golang-1.24-go_1.24.2-1_amd64.deb ...
Unpacking golang-1.24-go (1.24.2-1) ...
Selecting previously unselected package golang-1.24.
Preparing to unpack .../03-golang-1.24_1.24.2-1_all.deb ...
Unpacking golang-1.24 (1.24.2-1) ...
Selecting previously unselected package golang-src.
Preparing to unpack .../04-golang-src_2%3a1.24~2_all.deb ...
Unpacking golang-src (2:1.24~2) ...
Selecting previously unselected package golang-go:amd64.
Preparing to unpack .../05-golang-go_2%3a1.24~2_amd64.deb ...
Unpacking golang-go:amd64 (2:1.24~2) ...
Selecting previously unselected package golang-doc.
Preparing to unpack .../06-golang-doc_2%3a1.24~2_all.deb ...
Unpacking golang-doc (2:1.24~2) ...
Selecting previously unselected package golang:amd64.
Preparing to unpack .../07-golang_2%3a1.24~2_amd64.deb ...
Unpacking golang:amd64 (2:1.24~2) ...
Selecting previously unselected package libpkgconf3:amd64.
Preparing to unpack .../08-libpkgconf3_1.8.1-4_amd64.deb ...
Unpacking libpkgconf3:amd64 (1.8.1-4) ...
Selecting previously unselected package pkgconf-bin.
Preparing to unpack .../09-pkgconf-bin_1.8.1-4_amd64.deb ...
Unpacking pkgconf-bin (1.8.1-4) ...
Selecting previously unselected package pkgconf:amd64.
Preparing to unpack .../10-pkgconf_1.8.1-4_amd64.deb ...
Unpacking pkgconf:amd64 (1.8.1-4) ...
Setting up golang-1.24-src (1.24.2-1) ...
Setting up golang-1.24-doc (1.24.2-1) ...
Setting up libpkgconf3:amd64 (1.8.1-4) ...
Setting up golang-1.24-go (1.24.2-1) ...
Setting up pkgconf-bin (1.8.1-4) ...
Setting up golang-src (2:1.24~2) ...
Setting up golang-go:amd64 (2:1.24~2) ...
Setting up pkgconf:amd64 (1.8.1-4) ...
Setting up golang-1.24 (1.24.2-1) ...
Setting up golang-doc (2:1.24~2) ...
Setting up golang:amd64 (2:1.24~2) ...
Processing triggers for man-db (2.13.0-1) ...
Processing triggers for libc-bin (2.41-6ubuntu1) ...
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab09$ github-release --version
github-release: command not found
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab09$ export PATH=$PATH:~/go/bin
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab09$ github-release --version
github-release v0.10.1
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab09$ github-release info -u ${GITHUB_USERNAME} -r lab09
tags:
- v0.1.0.0 (commit: https://api.github.com/repos/YaQQrQ/lab09/commits/51ccb6339e3a377db46a51915431d4d32c9c7e41)
releases:
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab09$ github-release release \
> --user ${GITHUB_USERNAME} \
> --repo lab09 \
> --tag v0.1.0.0 \
> --name "libprint" \
>  --description "my first release"
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab09$ export PACKAGE_OS=`uname -s` PACKAGE_ARCH=`uname -m` 
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab09$ export PACKAGE_FILENAME=print-${PACKAGE_OS}-${PACKAGE_ARCH}.tar.gz
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab09$ github-release upload \
> --user ${GITHUB_USERNAME} \
> --repo lab09 \
> --tag v0.1.0.0 \
> --name "${PACKAGE_FILENAME}" \
> --file _build/*.tar.gz
Error: open _build/*.tar.gz: no such file or directory
Usage: github-release [global options] <verb> [verb options]

Global options:
        -h, --help                   Show this help
        -v, --verbose                Be verbose
        -q, --quiet                  Do not print anything, even errors (except if --verbose is specified)
            --version                Print version

Verbs:
    delete:
        -s, --security-token         Github token (required if $GITHUB_TOKEN not set)
        -u, --user                   Github repo user or organisation (required if $GITHUB_USER not set)
        -a, --auth-user              Username for authenticating to the API (falls back to $GITHUB_AUTH_USER or $GITHUB_USER)
        -r, --repo                   Github repo (required if $GITHUB_REPO not set)
        -t, --tag                    Git tag of release to delete (*)
    download:
        -s, --security-token         Github token ($GITHUB_TOKEN if set). required if repo is private.
        -u, --user                   Github repo user or organisation (required if $GITHUB_USER not set)
        -a, --auth-user              Username for authenticating to the API (falls back to $GITHUB_AUTH_USER or $GITHUB_USER)
        -r, --repo                   Github repo (required if $GITHUB_REPO not set)
        -l, --latest                 Download latest release (required if tag is not specified)
        -t, --tag                    Git tag to download from (required if latest is not specified) (*)
        -n, --name                   Name of the file (*)
    edit:
        -s, --security-token         Github token (required if $GITHUB_TOKEN not set)
        -u, --user                   Github repo user or organisation (required if $GITHUB_USER not set)
        -a, --auth-user              Username for authenticating to the API (falls back to $GITHUB_AUTH_USER or $GITHUB_USER)
        -r, --repo                   Github repo (required if $GITHUB_REPO not set)
        -t, --tag                    Git tag to edit the release of (*)
        -n, --name                   New name of the release (defaults to tag)
        -d, --description            New release description, use - for reading a description from stdin (defaults to tag)
            --draft                  The release is a draft
        -p, --pre-release            The release is a pre-release
    info:
        -s, --security-token         Github token ($GITHUB_TOKEN if set). required if repo is private.
        -u, --user                   Github repo user or organisation (required if $GITHUB_USER not set)
        -a, --auth-user              Username for authenticating to the API (falls back to $GITHUB_AUTH_USER or $GITHUB_USER)
        -r, --repo                   Github repo (required if $GITHUB_REPO not set)
        -t, --tag                    Git tag to query (optional)
        -j, --json                   Emit info as JSON instead of text
    release:
        -s, --security-token         Github token (required if $GITHUB_TOKEN not set)
        -u, --user                   Github repo user or organisation (required if $GITHUB_USER not set)
        -r, --repo                   Github repo (required if $GITHUB_REPO not set)
        -t, --tag                    Git tag to create a release from (*)
        -n, --name                   Name of the release (defaults to tag)
        -d, --description            Release description, use - for reading a description from stdin (defaults to tag)
        -c, --target                 Commit SHA or branch to create release of (defaults to the repository default branch)
            --draft                  The release is a draft
        -p, --pre-release            The release is a pre-release
        -g, --generate-release-notes Generate name and description if not given
    upload:
        -s, --security-token         Github token (required if $GITHUB_TOKEN not set)
        -u, --user                   Github repo user or organisation (required if $GITHUB_USER not set)
        -a, --auth-user              Username for authenticating to the API (falls back to $GITHUB_AUTH_USER or $GITHUB_USER)
        -r, --repo                   Github repo (required if $GITHUB_REPO not set)
        -t, --tag                    Git tag to upload to (*)
        -n, --name                   Name of the file (*)
        -l, --label                  Label (description) of the file
        -f, --file                   File to upload (use - for stdin) (*)
        -R, --replace                Replace asset with same name if it already exists (WARNING: not atomic, failure to upload will remove the original asset too)
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab09$ github-release info -u ${GITHUB_USERNAME} -r lab09
tags:
- v0.1.0.0 (commit: https://api.github.com/repos/YaQQrQ/lab09/commits/51ccb6339e3a377db46a51915431d4d32c9c7e41)
releases:
- v0.1.0.0, name: 'libprint', description: 'my first release', id: 215859917, tagged: 30/04/2025 at 19:49, published: 30/04/2025 at 20:00, draft: ✗, prerelease: ✗
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab09$ ls -la _build/*.tar.gz
ls: cannot access '_build/*.tar.gz': No such file or directory
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab09$ tar -czvf _build/package.tar.gz -C _build/ .
./
./Makefile
./CMakeFiles/
./CMakeFiles/TargetDirectories.txt
./CMakeFiles/3.31.6/
./CMakeFiles/3.31.6/CMakeCCompiler.cmake
./CMakeFiles/3.31.6/CMakeSystem.cmake
./CMakeFiles/3.31.6/CompilerIdC/
./CMakeFiles/3.31.6/CompilerIdC/CMakeCCompilerId.c
./CMakeFiles/3.31.6/CompilerIdC/a.out
./CMakeFiles/3.31.6/CompilerIdC/tmp/
./CMakeFiles/3.31.6/CMakeDetermineCompilerABI_C.bin
./CMakeFiles/3.31.6/CMakeCXXCompiler.cmake
./CMakeFiles/3.31.6/CompilerIdCXX/
./CMakeFiles/3.31.6/CompilerIdCXX/a.out
./CMakeFiles/3.31.6/CompilerIdCXX/tmp/
./CMakeFiles/3.31.6/CompilerIdCXX/CMakeCXXCompilerId.cpp
./CMakeFiles/3.31.6/CMakeDetermineCompilerABI_CXX.bin
./CMakeFiles/Makefile2
./CMakeFiles/Makefile.cmake
./CMakeFiles/progress.marks
./CMakeFiles/CMakeConfigureLog.yaml
./CMakeFiles/CMakeDirectoryInformation.cmake
./CMakeFiles/cmake.check_cache
./CMakeFiles/pkgRedirects/
./CMakeFiles/demo.dir/
./CMakeFiles/demo.dir/build.make
./CMakeFiles/demo.dir/compiler_depend.ts
./CMakeFiles/demo.dir/progress.make
./CMakeFiles/demo.dir/cmake_clean.cmake
./CMakeFiles/demo.dir/demo/
./CMakeFiles/demo.dir/link.txt
./CMakeFiles/demo.dir/DependInfo.cmake
./CMakeFiles/demo.dir/flags.make
./CMakeFiles/demo.dir/compiler_depend.make
./CMakeFiles/demo.dir/depend.make
./CMakeFiles/print.dir/
./CMakeFiles/print.dir/build.make
./CMakeFiles/print.dir/compiler_depend.ts
./CMakeFiles/print.dir/progress.make
./CMakeFiles/print.dir/cmake_clean.cmake
./CMakeFiles/print.dir/link.txt
./CMakeFiles/print.dir/DependInfo.cmake
./CMakeFiles/print.dir/flags.make
./CMakeFiles/print.dir/src/
./CMakeFiles/print.dir/compiler_depend.make
./CMakeFiles/print.dir/depend.make
./CMakeFiles/print.dir/cmake_clean_target.cmake
./CMakeFiles/CMakeScratch/
./CMakeCache.txt
./cmake_install.cmake
./_3rdParty/
./_3rdParty/Hunter/
./_3rdParty/Hunter/install-root-dir
./_3rdParty/Hunter/config-id/
./_3rdParty/Hunter/config-id/config.cmake
./_3rdParty/Hunter/config-id/config.cmake.NOLF
./_3rdParty/Hunter/toolchain/
./_3rdParty/Hunter/toolchain/toolchain.info.NOLF
./_3rdParty/Hunter/toolchain/toolchain.info
./_3rdParty/Hunter/toolchain/CMakeLists.txt
tar: .: file changed as we read it
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab09$ ls -la _build/*.tar.gz
-rw-rw-r-- 1 bari bari 53476 апр 30 20:06 _build/package.tar.gz
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab09$ github-release upload \
>     --user ${GITHUB_USERNAME} \
>     --repo lab09 \
>     --tag v0.1.0.0 \
>     --name "${PACKAGE_FILENAME}" \
>     --file _build/*.tar.gz
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab09$ github-release info -u ${GITHUB_USERNAME} -r lab09
tags:
- v0.1.0.0 (commit: https://api.github.com/repos/YaQQrQ/lab09/commits/51ccb6339e3a377db46a51915431d4d32c9c7e41)
releases:
- v0.1.0.0, name: 'libprint', description: 'my first release', id: 215859917, tagged: 30/04/2025 at 19:49, published: 30/04/2025 at 20:00, draft: ✗, prerelease: ✗
  - artifact: print-Linux-x86_64.tar.gz, downloads: 0, state: uploaded, type: application/octet-stream, size: 54 kB, id: 250828423
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab09$ wget https://github.com/${GITHUB_USERNAME}/lab09/releases/download/v0.1.0.0/${PACKAGE_FILENAME}
--2025-04-30 20:07:51--  https://github.com/YaQQrQ/lab09/releases/download/v0.1.0.0/print-Linux-x86_64.tar.gz
Resolving github.com (github.com)... 140.82.121.3
Connecting to github.com (github.com)|140.82.121.3|:443... connected.
HTTP request sent, awaiting response... 302 Found
Location: https://objects.githubusercontent.com/github-production-release-asset-2e65be/975717899/f084a35e-27c3-4ffd-a7a6-1b7fbc7d377a?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=releaseassetproduction%2F20250430%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20250430T200751Z&X-Amz-Expires=300&X-Amz-Signature=10b2ed9bd75a553195f58e689c2ef2c5940aaecddfe9cff372bb710cea7d8dc8&X-Amz-SignedHeaders=host&response-content-disposition=attachment%3B%20filename%3Dprint-Linux-x86_64.tar.gz&response-content-type=application%2Foctet-stream [following]
--2025-04-30 20:07:51--  https://objects.githubusercontent.com/github-production-release-asset-2e65be/975717899/f084a35e-27c3-4ffd-a7a6-1b7fbc7d377a?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=releaseassetproduction%2F20250430%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20250430T200751Z&X-Amz-Expires=300&X-Amz-Signature=10b2ed9bd75a553195f58e689c2ef2c5940aaecddfe9cff372bb710cea7d8dc8&X-Amz-SignedHeaders=host&response-content-disposition=attachment%3B%20filename%3Dprint-Linux-x86_64.tar.gz&response-content-type=application%2Foctet-stream
Resolving objects.githubusercontent.com (objects.githubusercontent.com)... 185.199.108.133, 185.199.109.133, 185.199.110.133, ...
Connecting to objects.githubusercontent.com (objects.githubusercontent.com)|185.199.108.133|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 53476 (52K) [application/octet-stream]
Saving to: ‘print-Linux-x86_64.tar.gz’

print-Linux-x86_64.tar.gz   100%[==========================================>]  52,22K  --.-KB/s    in 0,03s   

2025-04-30 20:07:52 (1,92 MB/s) - ‘print-Linux-x86_64.tar.gz’ saved [53476/53476]

bari@ubuntu24:~/YaQQrQ/workspace/projects/lab09$ tar -ztf ${PACKAGE_FILENAME}
./
./Makefile
./CMakeFiles/
./CMakeFiles/TargetDirectories.txt
./CMakeFiles/3.31.6/
./CMakeFiles/3.31.6/CMakeCCompiler.cmake
./CMakeFiles/3.31.6/CMakeSystem.cmake
./CMakeFiles/3.31.6/CompilerIdC/
./CMakeFiles/3.31.6/CompilerIdC/CMakeCCompilerId.c
./CMakeFiles/3.31.6/CompilerIdC/a.out
./CMakeFiles/3.31.6/CompilerIdC/tmp/
./CMakeFiles/3.31.6/CMakeDetermineCompilerABI_C.bin
./CMakeFiles/3.31.6/CMakeCXXCompiler.cmake
./CMakeFiles/3.31.6/CompilerIdCXX/
./CMakeFiles/3.31.6/CompilerIdCXX/a.out
./CMakeFiles/3.31.6/CompilerIdCXX/tmp/
./CMakeFiles/3.31.6/CompilerIdCXX/CMakeCXXCompilerId.cpp
./CMakeFiles/3.31.6/CMakeDetermineCompilerABI_CXX.bin
./CMakeFiles/Makefile2
./CMakeFiles/Makefile.cmake
./CMakeFiles/progress.marks
./CMakeFiles/CMakeConfigureLog.yaml
./CMakeFiles/CMakeDirectoryInformation.cmake
./CMakeFiles/cmake.check_cache
./CMakeFiles/pkgRedirects/
./CMakeFiles/demo.dir/
./CMakeFiles/demo.dir/build.make
./CMakeFiles/demo.dir/compiler_depend.ts
./CMakeFiles/demo.dir/progress.make
./CMakeFiles/demo.dir/cmake_clean.cmake
./CMakeFiles/demo.dir/demo/
./CMakeFiles/demo.dir/link.txt
./CMakeFiles/demo.dir/DependInfo.cmake
./CMakeFiles/demo.dir/flags.make
./CMakeFiles/demo.dir/compiler_depend.make
./CMakeFiles/demo.dir/depend.make
./CMakeFiles/print.dir/
./CMakeFiles/print.dir/build.make
./CMakeFiles/print.dir/compiler_depend.ts
./CMakeFiles/print.dir/progress.make
./CMakeFiles/print.dir/cmake_clean.cmake
./CMakeFiles/print.dir/link.txt
./CMakeFiles/print.dir/DependInfo.cmake
./CMakeFiles/print.dir/flags.make
./CMakeFiles/print.dir/src/
./CMakeFiles/print.dir/compiler_depend.make
./CMakeFiles/print.dir/depend.make
./CMakeFiles/print.dir/cmake_clean_target.cmake
./CMakeFiles/CMakeScratch/
./CMakeCache.txt
./cmake_install.cmake
./_3rdParty/
./_3rdParty/Hunter/
./_3rdParty/Hunter/install-root-dir
./_3rdParty/Hunter/config-id/
./_3rdParty/Hunter/config-id/config.cmake
./_3rdParty/Hunter/config-id/config.cmake.NOLF
./_3rdParty/Hunter/toolchain/
./_3rdParty/Hunter/toolchain/toolchain.info.NOLF
./_3rdParty/Hunter/toolchain/toolchain.info
./_3rdParty/Hunter/toolchain/CMakeLists.txt

