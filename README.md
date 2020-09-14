
# Cleaned up Quake id1 v1.01 QuakeC source

Because of vagueness with licensing, v1.06 source isn't necessarily a good place to start from. v1.01 is more explicitely released under GPL in the quake-tools source release by id software.

I've redone a few of the fixes that were also done in v1.06, but not all of them, there's a few multiplayer specific ones that I didn't bother with (mostly killmessages). 

I would recommend using a modern compiler like FTEQCC or gmqcc etc. 

My changes done to the codebase compared to v1.01:
- Eliminate all warnings that FTEQCC gives it
- Fix parm7 not being set to 0 properly in SetNewParms (cells) (like in v1.06)
- Remove DumpScore (like in v1.06)
- Prioritize other kill messages over liquid deaths(so monster killing you in water doesn't print drowning message) (like in v1.06)
- Add prev weapon command (like in v1.06)
- Fix fish count
- Remove all of the "local" keywords that are not used by any relevant compiler
- Lots of automatic and manual syntax cleanup
  - Consistent spacing for frame macros
  - Consistent use of whitespace
  - Consistent spacing around and inside () and {}
  - Try to eliminate mixed indentation (using 4-size tabs as suggested by original sources)
