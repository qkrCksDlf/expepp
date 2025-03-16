# expepp

```export CUDA_VISIBLE_DEVICES="0"
export MODLE="zcaoyao/Flower_Concept "
export SOURCE_MASK="./example/bbox.jpg"
export SOURCE_IMAGE="./example/example_image.jpg"
export OUTPUT_DIR="./example/flower"
python InstantSwap.py \
    --model_id $MODLE \
    --source_mask $SOURCE_MASK \
    --source_image $SOURCE_IMAGE \
    --source_prompt " " \
    --target_prompt "sks flower" \
    --diff_prompt "sks flower" \
    --diff_prompt_source "shell" \
    --guidance_scale 7.5 \
    --output $OUTPUT_DIR \
    --interval 5 \
    --iters 550



```export MODLE="stabilityai/stable-diffusion-2-1-base"
export SOURCE_IMAGE="./example_image.jpg"
export OUTPUT_DIR="./example"
python get_bbox.py \
    --model_id $MODLE \
    --source_image $SOURCE_IMAGE \
    --source_prompt "a person holding a shell in front of the ocean" \
    --guidance_scale 3 \
    --word_idx 5 \
    --output $OUTPUT_DIR \
    --iters 3

