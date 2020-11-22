Git Commit Tag Examples

- feat: a new feature for the user, not a new feature for a build script
- fix: bug fix for the user, not a fix to a build scripts
- refactor: refactoring production code
- chore: updating gulp tasks etc.; no production code change
- docs: changes to documentation
- style: formatting, missing semicolons, etc.; no code change
- perf: code improved in terms of processing performance
- vendor: update version for dependencies, packages.
- test: adding missing tests, refactoring tests; no production code
- yukarıda belirtilen kategoriler ile başlayan kaçartane commit olduğunu sayan komut


git log --pretty=oneline --no-merges | cut -d " " -f 2 | grep -e 'feat:' -e 'fix:' -e 'refactor:' -e 'chore:' -e 'docs:' -e 'style:' -e 'perf:' -e 'vendor:' -e 'test:' |\
cut -d "(" -f 1 | cut -d ":" -f 1 | sort -r | uniq -c | sort -nr -k1