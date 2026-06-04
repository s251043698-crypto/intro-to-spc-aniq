library(ggplot2)
library(plotly)

plot_math_vs_gender <- ggplot(bigclass, aes(x = sex, y = Math, fill = sex)) +
    geom_boxplot(outlier.colour = "red", outlier.shape = 8, outlier.size = 2) +
    scale_fill_manual(values = c("#0072B2", "#D55E00")) +
    labs(
        title = "Math Scores by Gender in bigclass Dataset",
        x = "Gender",
        y = "Math Score"
    ) +
    theme_minimal() +
    theme(
        plot.background = element_rect(fill = "white", colour = NA),
        panel.background = element_rect(fill = "white", colour = NA),
        axis.title.x = element_text(size = 18),
        axis.title.y = element_text(size = 18),
        axis.text.x = element_text(size = 14),
        axis.text.y = element_text(size = 14),
        legend.position = "none"
    )

plotly_math_vs_gender <- ggplotly(plot_math_vs_gender)
