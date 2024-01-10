Made in 2022.3.15f1

I've spent about 6 hours in total. 2 hours setting up the bulk of the shader graph. 3 hours fiddling with the settings and adjusting specific values, adjusting textures in Substance Designer. About 1 hour for the texture and VFX graph for the drips below the box.

The main material has been made with three single channel texture (could've packed them).
I'm using some UV math to offset and move the main rain flow/drips. Lerping them based on a simple noise.

The splashes become visible based on a voronoi noise that fits one drip in each cell. That way I can offset the time I use to fade in/out the splashes.
Based on the vertex normal I lerp between the splashes that would drip on a floor/roof and the flow of water on walls/edges, I offset it a little so there's also some minimal splashes on the walls.

The drips below the box are fairly simple. It's just drips.
All textures are made in Substance Designer.
I've opted to not bake normals and blend those for sake of simplicity. I think doing the Normal From Height once at the end is cheaper than 3 or 4 normal texture samplers.
I've thought about making a render target that has a VFX rendered into it for simulating the rain, but that would be fairly expensive and possibly hard to make tiling.

Given more time I would see if I can layer the rain better, and specifically make a better rain texture. I'm not sure how that texture would need to look exactly, this was the first time I've had to make rain. I would definitely do some more research and find more reference.

