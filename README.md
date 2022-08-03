# TopEFT
Cards for gridpack generation in MadGraph

=======

## Naming 

'01j' indicates an extra jet
'01jq' indicates an extra jet, where the jet cannot be a b or b~ although 5f scheme is used
'1l_wm' inidcates that all w- are decaying leptonically and all w+ hadronically
'1l_mp' inidcates that all w+ are decaying leptonically and all w- hadronically
'dilep' indicates that both W- and w+ decay leptonically
'1l' in the single top t-channel there is only one w per event and this decays leptonically
'4f' implemented in the 4f scheme (all processes without this are 5f scheme)

 
## MadSpin and decays

All madspin cards are deactivated but they are still in the directories. 
If the madspin cards are deactivated, there is no w decay and thus '1l_wm', '1l_wp' and 'dilep' all give the same result which is inclusive over all w decays.


## Problems

tW01j-1l-wm, tW01j-1l-wp and tW01j-dilep give an error in the reweighting procedure in the subprocess b b~ > b w+ b~ w-.
Thus, also the versions without extra jets (tW), in the 4f scheme (tW01j-4f) and a version where the extra jet cannot be a b (tW01jq) are implemented.
In those three special version, no madspin card is provided.
