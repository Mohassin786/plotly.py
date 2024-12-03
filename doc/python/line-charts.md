# Re-creating the graph with updated legend text
plt.figure(figsize=(10, 6))
plt.plot(stages, sales, marker='o', linestyle='-', color='blue', linewidth=2, label='Sales Trend')
plt.title("Product Life Cycle of Nintendo Switch in the USA", fontsize=14, fontweight='bold')
plt.xlabel("PLC Stages", fontsize=12)
plt.ylabel("Sales (in Million Units)", fontsize=12)
plt.grid(alpha=0.5, linestyle='--')
plt.xticks(fontsize=10)
plt.yticks(fontsize=10)
plt.legend(fontsize=10)
plt.tight_layout()

# Highlight the trend line
plt.fill_between(stages, sales, color='blue', alpha=0.1)

# Annotate sales units
for i, (x, y) in enumerate(zip(stages, sales)):
    plt.text(x, y + 0.2, f"{y:.2f}M", color="black", fontsize=10, ha='center')

# Save the updated graph as an image file
updated_image_path = "/mnt/data/Nintendo_Switch_PLC_Sales_Trend.png"
plt.savefig(updated_image_path)

updated_image_path
