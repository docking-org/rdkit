rdkit_python_extension(rdSubstructLibrary
                       rdSubstructLibrary.cpp
                       SubstructLibraryWrap.cpp
                       DEST Chem
                       LINK_LIBRARIES
                       SubstructLibrary
Fingerprints SubstructMatch SmilesParse Catalogs FileParsers GraphMol DataStructs
RDGeometryLib RDGeneral RDBoost
)

add_pytest(pySubstructLibrary ${CMAKE_CURRENT_SOURCE_DIR}/rough_test.py)
