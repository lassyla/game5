
BLENDER="C:\Program Files\Blender Foundation\Blender 2.90\blender.exe"
DIST=../dist

all : \
    $(DIST)/corn.pnct \
    $(DIST)/corn.scene \
	$(DIST)/corn.w \

$(DIST)/corn.scene : corn.blend export-scene.py
    $(BLENDER) --background --python export-scene.py -- "corn.blend:Platforms" "$(DIST)/corn.scene"

$(DIST)/corn.pnct : corn.blend export-meshes.py
    $(BLENDER) --background --python export-meshes.py -- "corn.blend:Platforms" "$(DIST)/corn.pnct" 

$(DIST)/corn.w : corn.blend export-walkmeshes.py
    $(BLENDER) --background --python export-walkmeshes.py -- "corn.blend:WalkMeshes" "$(DIST)/corn.w" 
