# expepp

```
export CUDA_VISIBLE_DEVICES="0"
export MODLE="Carmen000/dreambooth_candle"
export SOURCE_MASK="./example/bbox.jpg"
export SOURCE_IMAGE="./example/example_image.jpg"
export OUTPUT_DIR="./example/flower"
python InstantSwap.py \
    --model_id $MODLE \
    --source_mask $SOURCE_MASK \
    --source_image $SOURCE_IMAGE \
    --source_prompt "candle" \
    --target_prompt "a sks candle" \
    --diff_prompt "a sks candle" \
    --diff_prompt_source "a sks candle" \
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
    --source_prompt "candle" \
    --guidance_scale 3 \
    --word_idx 5 \
    --output $OUTPUT_DIR \
    --iters 3
```
