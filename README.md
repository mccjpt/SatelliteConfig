# SatelliteConfig

Git repository demonstrating how MetaEdit+ supports the Model Management Challenge 2025 (https://doi.org/10.5281/zenodo.15285132). Each scenario from the MoM challenge is its own version in Git, and MoM challenge starts from having version 1 made. 

The modeling solution presented enables collaborative simultaneous work directly in high-level models, minimizes the effort of modeling and integration, provides fast feedback on changes, keeps artefacts consistent, traceable and up-to-date, and provides hassle-free versioning. 

## Quick Start

**To see the how MetaEdit+ supports merge-free collaborative modeling with user-defined domain-specific modeling languages:**

1. Install MetaEdit+ from https://metacase.com/download/

2. Download the intial MetaEdit+ repository version, the binary file asset [SatAlphaVersion1.zip](https://github.com/mccjpt/SatelliteConfig/releases/download/1/SatAlphaVersion1.zip) from Release 1 here.

3. Expand SatAlphaVersion1.zip to form a new SatAlphaVersion1 folder in your MetaEdit+ working directory (e.g. Documents\MetaEdit+ 5.5)

4. Start MetaEdit+, select the new 'SatAlphaVersion1' repository and 'SatAlpha' project. For login there are four different users available: user 'config' with password 'config' defines the configurations and requirements, and 'antenna', 'solar' and 'thurster' manage the components in parts catalogue and create views.

For more details about satellite configuration scenarios, see the MoM challenge in https://doi.org/10.5281/zenodo.15285132

The repository provided for MetaEdit+ can be used in both single-user and multi-user versions, the latter offering simultaneous collaborative modeling. The instructions given here are for single-user MetaEdit+, and details about multi-user version are outlined in https://www.metacase.com/mep/multi-user.html and detailed in MetaEdit+ User’s Guides.

## Extra: Full Git History

**Experienced users can link MetaEdit+ to GitHub and access the state of the repository after various scenarios.**

1. Install MetaEdit+. 
MetaEdit+ user guide is available at https://metacase.com/support/55/manuals/ and integration with version control systems (VCS) is detailed in https://metacase.com/support/55/manuals/meplus/Mp-3_5.html. 

2. Fork the https://github.com/mccjpt/SatelliteConfig repository into your own VCS online. For simplicity, we'll assume your online VCS platform is GitHub and user name there is GITUSER.

3. Create a directory and settings for Git integration. For simplicity, we'll assume your local OS is Windows and user name is OSUSER.
   - In your MetaEdit+ working directory (by default C:\Users\OSUSER\Documents\MetaEdit+ 5.5), `mkdir git`. 
   - Add this new directory and _your_ GitHub account URL (without /SatelliteConfig suffix) to a `.vcsPaths` file in your MetaEdit+ working directory:

        ```
        gitBaseDir=C:\Users\OSUSER\Documents\MetaEdit+ 5.5\git
        gitBaseURL=https://github.com/GITUSER
        ```
4. Make a local clone of your fork. Run the following in a command prompt in your MetaEdit+ working directory, adjusting the location of the MetaEdit+ executable as necessary:

    ```
    set metaedit="C:\Program Files (x86)\MetaEdit+ 5.5\mep55.exe" fileInPatches
    %metaedit% textForMERL: "_vcsInitClone('SatelliteConfig')" logoutAndExit
    git config -f git\SatelliteConfig\.git\config --unset core.sharedRepository
    ```

    You'll be prompted for your GitHub password, and assuming all goes well you can close the command prompt at the end. (The last line is just to avoid a [bug](https://github.com/git-for-windows/git/issues/3110) in Git for Windows.)

4. Start MetaEdit+, select the 'SatelliteConfig' repository and 'SatAlpha' project, and Login. 
You can now seen the latest version where all four engineers have collaboratively created SatAlpha version 2.  

## Inspecting model management scenarios individually
To see or conduct any particular scenario, checkout the version from your Git
1. Choose **Repository | Changes & Versions** and then checkout the desired version by selecting **Extra VCS Commands | CheckOut**. 
2. Enter the name for the new MetaEdit+ repository to be created (e.g. the name of the scenario, like SatelliteConfigAfter1). 
3. Enter the Git hash for the desired version (version 0's hash to start from the beginning, version 1's hash for version 1 etc.).
   - MetaEdit+ starts and opens the repository asking for login password. Open the project to try out the desired MoM scenario.

_You can ignore Git's "detached head" warning: your local Git has already moved back to the latest version, matching your separate original SatelliteConfig MetaEdit+ repository._

## Prerequisites
MetaEdit+ 5.5 SR1, https://metacase.com/download
