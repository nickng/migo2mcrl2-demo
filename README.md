# migo2mcrl2-demo

Demo files for MiGo types to mCRL2 generation.

## Pre-requisites

 - Everything runs off Docker
 - Network connection to view [slides](https://drive.google.com/open?id=1o1Mkhrf_av1u52lKu-7lJe0MolrLT8Tf1wBLA8acpGg) on Google Drive

## Files

 - `http-demo` runs the web demo locally (use `CTRL-C` to quit)
 - `run-docker` executes commands inside the docker container,
    e.g. `run-docker /bin/sh` runs an interactive shell
 - `CHEATSHEET` contains the commands to manually check a given mCRL2 file for
   easy copy-and-paste

## Run

To run demo manually (checks for deadlock freedom for `deadlock.migo`)

    ./run-docker Godel deadlock.migo # Generates model and formulae
    ./run-docker mcrl22lps model.crl2 model.crl2.lps
    ./run-docker lps2pbes --formula=formula-df.mcf model.crl2.lps model.crl2.lps.pbes
    ./run-docker pbes2bool model.crl2.lps.pbes
