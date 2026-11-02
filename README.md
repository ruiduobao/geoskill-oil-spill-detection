# geoskill-oil-spill-detection

> SAR 暗斑油膜检测 — 从 SAR 暗斑中筛选疑似油膜，结合风场、形状、纹理、船舶和自然 slick 线索 输出人工复核候选。支持后向散射阈值分割、多特征融合置信度评分与误报过滤。

See [SKILL.md](SKILL.md) for full usage, inputs and outputs.

## Quick start

```bash
# 合成演示模式（无需输入文件）
python scripts/oil_spill_detection.py --output-dir ./osd-output

# 指定检测方法
python scripts/oil_spill_detection.py --method threshold_adaptive --output-dir ./osd-output

# 自定义最小面积和置信度阈值
python scripts/oil_spill_detection.py --min-area 2000.0 --confidence-threshold 0.5 --output-dir ./osd-output

# 自适应阈值分割
python scripts/oil_spill_detection.py --method threshold_adaptive --grid-size 200 --output-dir ./osd-output
```

## License

MIT
