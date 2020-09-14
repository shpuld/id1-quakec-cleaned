
# Cleaned up Quake id1 v1.01 QuakeC source

This is just the QuakeC source for vanilla Quake for modders to use.

Because of vagueness with licensing, Quake 1.06 source isn't necessarily a good place to start from, it did not come with any license attached. Meanwhile 1.01 is more explicitely released under GPL in the Quake-Tools source release by id software: https://github.com/id-Software/Quake-Tools

Anyone who has done QuakeC programming knows how messy the codebase is, and that there's some known bugs there too. While I've avoided changing the code behavior, I've done a lot of very basic clean up and fixed more harmless bugs (Rotfish monster count anyone?). The major changes from v1.06 have been redone here, but there's a few multiplayer specific things in v1.06 that are not in this release (mostly killmessages). 

My changes done to the codebase compared to 1.01:
- Eliminate all warnings that FTEQCC gives it
- Fix parm7 not being set to 0 properly in SetNewParms (cells) (like in v1.06)
- Remove DumpScore (like in v1.06)
- Prioritize other kill messages over liquid deaths(so monster killing you in water doesn't print drowning message) (like in v1.06)
- Add prev weapon command (like in v1.06)
- Fix fish monster count
- Remove all of the "local" keywords that are not used by any relevant compiler (if your compiler refuses to compile without it, use a newer compiler)
- Lots of automatic and manual syntax cleanup
  - Consistent spacing for frame macros
  - Consistent use of whitespace
  - Consistent spacing around and inside () and {}
  - Try to eliminate mixed indentation (using 4-size tabs as suggested by original sources)
