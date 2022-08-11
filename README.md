# TopEFT
Cards for gridpack generation in MadGraph

## Naming 

'01j' indicates an extra jet

'01jq' indicates an extra jet, where the jet cannot be a b or b~ although 5f scheme is used

'dilep' indicates that both w- and w+ decay leptonically

'1l' in the single top t-channel there is only one w per event and this decays leptonically

'4f' implemented in the 4f scheme (all processes without this are 5f scheme), this also means that the 4f restriction card is loaded and maxflavor=4 in run card

 
## Decays

Decays of top and W are performed in the process command including SM-EFT effects. Widths are updated automatically for each base point during reweighting.

## Creation of reweight card including decay:

python make_reweight_card.py --couplings 2 cHG 1 cHGtil 1 cHj1 1 cHj3 1 cHu 1 cHd 1 cHQ3 1 cHtbRe 1 cHtbIm 1 cHW 1 cHWtil 1 cHB 1 cHBtil 1 cHWB 1 cHWBtil 1 cHbox 1 cHDD 1 cHl3 1 cll1 1 cG 1 cGtil 1 ctGRe 1 ctGIm 1 ctWRe 1 ctWIm 1 --filename BIT_reweight_card.dat --overwrite --auto_width_particles 6 24

## Problems

tW01j-1l-wm, tW01j-1l-wp and tW01j-dilep give an error in the reweighting procedure in the subprocess b b~ > b w+ b~ w-.
Thus, also the versions without extra jets (tW), in the 4f scheme (tW01j-4f) and a version where the extra jet cannot be a b (tW01jq) are implemented.
In those three special version, no madspin card is provided.

## Gridpack location 

With W-decay in proc_card: /eos/user/c/chatterj/HiggsEFT/BITv3/Gridpacks/w_W_decay/  (on lxplus)
 
Without W-decay in proc_card: /eos/user/c/chatterj/HiggsEFT/BITv3/Gridpacks/ (on lxplus)
