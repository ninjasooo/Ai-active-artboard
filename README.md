# Ai-active-artboard
make a specific artboard as active on adobe illustrator

var docRef = app.activeDocument;
var ABName = "Artboard 3";
function setActiveArtboardBy(name) {
    var artboard = docRef.artboards.getByName(name);
    for (i = 0; i < docRef.artboards.length; i++) {
        if (docRef.artboards[i] == artboard) {
            docRef.artboards.setActiveArtboardIndex(i);
            break;
        }
    }
}
setActiveArtboardBy(ABName);
