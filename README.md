# LHE->NanoGen script

To set up in a new CMSSW area:
```bash
cmsrel CMSSW_10_6_19_patch2
cd CMSSW_10_6_19_patch2/src
cmsenv
mkdir Configuration
git clone https://github.com/pieterdavid/NanoGenScripts.git -o Configuration/NanoGenScripts
scram b
```
or inside an existing CMSSW area
```bash
cd $CMSSW_BASE/src
mkdir -p Configuration
git clone https://github.com/pieterdavid/NanoGenScripts.git -o Configuration/NanoGenScripts
scram b
```

Run as follows:
```
./Configuration/NanoGenScripts/lheToNanoGen.sh <fragment> <lhe> <output>
```
where `<fragment>` is a fragment with an externalLHEProducer and hadronizer settings compatible with the process in the LHE file.
