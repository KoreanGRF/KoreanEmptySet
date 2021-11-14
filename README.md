# Korean Empty Set
**Korean Empty Set**은 한국 관련 NewGRF 세트를 위한 템플릿입니다.  
**Korean Empty Set** is a template for Korean NewGRF sets.

# Requires
You need Linux bash shell or WSL to make your NewGRF project by using this template.

# How to use
 1. Modify ``Makefile.config``. Do not modify other variables if there is no certain purpose.
    ```
    # Name
    REPO_NAME           ?= Korean Empty Set
    
    # File name of *.grf, *.tar and so on
    BASE_FILENAME       ?= ko_empty_set
    
    # Versin
    VERSION             ?= $(shell ./findversion.sh)
    RECENT_UPDATED      ?= $(shell date +"%Y.%m.%d")
    REPO_BRANCH_VERSION ?= 0
    
    # Author's information
    AUTHOR_WEBSITE      ?= https://domain.com
    AUTHOR_EMAIL        ?= your_email@address.com
    
    # If needed, declare the minimum NML requirements
    REQUIRED_NML_BRANCH  = 0.4
    # MIN_NML_REVISION   = 0
    ```
    * ``REPO_NAME``: Your NewGRF name  
    * ``BASE_FILENAME``: Your NewGRF's file name
    * ``AUTHOR_WEBSITE``: NewGRF's website url
    * ``AUTHOR_EMAIL``: Author's email address
 2. Modify ``license.txt`` and ``readme.ptxt`` as you wish
 3. Rename ``ko_empty_set.pnml`` into the ``(BASE_FILENAME).grf``  
    (eg. if ``BASE_FILENAME`` is _ko_test_grf_, then rename it into _ko_test_grf.grf_)
 4. Write your code in ``(BASE_FILENAME).grf``.  
    You may put some other _.pnml_ files by creating some directories, such as ``src``.  
	Then you may include it by ``#include "./src/some_file_name.pnml"`` syntax.
 5. Run ``make all`` in the shell. Then compiled tar file generated in **_./generated/+** directory.
 6. ``make clean`` will clean your project.
