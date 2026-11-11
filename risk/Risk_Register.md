import matplotlib.pyplot as plt
from matplotlib.patches import Rectangle

# Risk data
risks = {
    "R1": (4, 4),
    "R2": (4, 5),
    "R3": (3, 5),
    "R4": (3, 4),
    "R5": (3, 5),
    "R6": (5, 3),
    "R7": (3, 5),
    "R8": (3, 5),
    "R9": (3, 4),
    "R10": (2, 5)
}

fig, ax = plt.subplots(figsize=(9, 7))

# Risk matrix colors
matrix = [
    ["#8BC34A", "#8BC34A", "#CDDC39", "#FFEB3B", "#FFC107"],
    ["#8BC34A", "#CDDC39", "#FFEB3B", "#FFC107", "#FF9800"],
    ["#CDDC39", "#FFEB3B", "#FFC107", "#FF9800", "#F44336"],
    ["#FFEB3B", "#FFC107", "#FF9800", "#F44336", "#D32F2F"],
    ["#FFC107", "#FF9800", "#F44336", "#D32F2F", "#B71C1C"]
]

# Draw cells
for impact in range(1, 6):
    for likelihood in range(1, 6):
        ax.add_patch(
            Rectangle(
                (likelihood - 0.5, impact - 0.5),
                1,
                1,
                facecolor=matrix[impact - 1][likelihood - 1],
                edgecolor="white",
                linewidth=2
            )
        )

# Plot risks
for risk, (likelihood, impact) in risks.items():
    ax.scatter(
        likelihood,
        impact,
        s=500,
        color="#263238",
        zorder=5
    )

    ax.text(
        likelihood,
        impact,
        risk,
        color="white",
        ha="center",
        va="center",
        fontsize=9,
        fontweight="bold",
        zorder=6
    )

# Formatting
ax.set_xlim(0.5, 5.5)
ax.set_ylim(0.5, 5.5)

ax.set_xticks(range(1, 6))
ax.set_yticks(range(1, 6))

ax.set_xlabel(
    "Likelihood",
    fontsize=12,
    fontweight="bold"
)

ax.set_ylabel(
    "Impact",
    fontsize=12,
    fontweight="bold"
)

ax.set_title(
    "ReWire.U Cybersecurity Risk Heat Map",
    fontsize=16,
    fontweight="bold",
    pad=20
)

# Clean look
for spine in ax.spines.values():
    spine.set_visible(False)

ax.tick_params(length=0)
ax.set_facecolor("white")

plt.tight_layout()

plt.savefig(
    "Risk_Heat_Map.png",
    dpi=300,
    bbox_inches="tight"
)

plt.show()
