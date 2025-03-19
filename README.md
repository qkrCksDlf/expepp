# expepp

```
export CUDA_VISIBLE_DEVICES="0"
export MODLE="sd-dreambooth-library/the-witcher-game-ciri"
export SOURCE_MASK="./example/bbox.jpg"
export SOURCE_IMAGE="./example/example_image.jpg"
export OUTPUT_DIR="./example/flower"
python InstantSwap.py \
    --model_id $MODLE \
    --source_mask $SOURCE_MASK \
    --source_image $SOURCE_IMAGE \
    --source_prompt "head" \
    --target_prompt "a sks woman with white hair head" \
    --diff_prompt "a sks woman with white hair head" \
    --diff_prompt_source "a sks woman with white hair head" \
    --guidance_scale 7.5 \
    --output $OUTPUT_DIR \
    --interval 5 \
    --iters 550
```


```
export MODLE="stabilityai/stable-diffusion-2-1-base"
export SOURCE_IMAGE="./example_image.jpg"
export OUTPUT_DIR="./example"
python get_bbox.py \
    --model_id $MODLE \
    --source_image $SOURCE_IMAGE \
    --source_prompt "a heart candy" \
    --guidance_scale 3 \
    --word_idx 5 \
    --output $OUTPUT_DIR \
    --iters 3
```
