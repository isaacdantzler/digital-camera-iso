The question that started this: in the studio, on the worse cameras, dropping ISO visibly cleans up the picture. But everyone says ISO doesn't cause noise. Both are true.

Interactive version: open `iso-lab.html` in the repo root in a browser. It simulates a sensor so you can change ISO with and without changing the light.

Summary:
- A sensor's sensitivity is fixed. ISO does not change how much light the pixels catch.
- Most noise is the light itself (photon shot noise). Count N photons and the noise is √N, so more light = cleaner. 4x the light is 2x cleaner.
- ISO is gain applied *after* capture. It multiplies the signal and the noise already in it by the same amount.
- Lowering ISO makes the picture darker, so you (or auto exposure) add light, open the aperture, or slow the shutter. **That extra light is what removes the noise.**
- The one real advantage of low ISO: at base ISO the pixels can fill completely before clipping, so it lets you use the most light.

The counterintuitive part:
- Hold the light fixed and change only ISO, and lower ISO is *not* cleaner. On older sensors it is worse, because the noise added by the converter after the gain stage is no longer small next to the signal.
- So don't shoot dark at low ISO and lift it in the edit on older cameras. Use the higher ISO.
- Newer sensors add very little noise after the gain stage, so at fixed light the ISO setting barely matters ("ISO-invariant"). Higher ISO just costs highlight headroom.
- Dual native ISO cameras switch to a second, quieter readout circuit at the higher base. Just above that point is cleaner than just below it.

Why the bad cams show it most:
- Small sensors gather less total light at the same f-stop and framing, so they start noisier.
- Webcams and auto modes raise gain silently when light is short. Adding light makes them drop it again.

Ties back to [[ISO 12232]]: the standard defines ISO by how bright the output image is for a given exposure, not by sensor sensitivity. It is a label for how much light to supply. On film ([[Film Speed]]) a faster stock really was a different, grainier emulsion, which is where blaming the number comes from.
