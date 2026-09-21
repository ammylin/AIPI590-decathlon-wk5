{
      "cell_type": "markdown",
      "metadata": {},
      "source": [
        "## Results Table\n",
        "\n",
        "Edit this markdown cell as you work through the events. Keep each evidence claim short enough that someone else can understand what your method showed and why you assigned the medal.\n",
        "\n",
        "**My assigned method:** Counterfactual explanations\n",
        "\n",
        "| Event | Question | Medal | Evidence from my method | Limitations or notes |\n",
        "|---|---|---|---|---|\n",
        "| 1. Most Important Feature | What variable most strongly influences the tabular model's predictions? | TODO |  |  |\n",
        "| 2. One Specific Prediction | Why did this individual tabular prediction occur? | Silver | For local row 718, changing only `debt_ratio` from 0.281 to 0.283 changed the model from low risk (`P=0.499`) to high risk (`P=0.502`). | The case is extremely close to the decision boundary. Counterfactuals show model sensitivity, not causality. |\n",
        "| 3. Dataset Bias or Shortcut | Is the image model relying on a spurious shortcut? | TODO |  |  |\n",
        "| 4. Global Feature Effect | As one tabular feature changes, what happens to predictions? | TODO |  |  |\n",
        "| 5. Compare Two Predictions | Why were two cases classified differently? | Gold | The high-risk case had `P=0.789` versus `0.022` for the low-risk case. Replacing one feature at a time showed that `debt_ratio` (`+0.147`) and `recent_late_payments` (`+0.103`) contributed the largest probability increases. | One-feature interventions isolate effects but do not capture feature interactions or prove causality. |\n",
        "| 6. Feature Interactions | Which tabular variables work together? | TODO |  |  |\n",
        "| 7. Where Is the Model Looking? | What region of an image drives the prediction? | TODO |  |  |\n",
        "| 8. Explain a Failure | Why did the model make this mistake? | Silver | Failure row 1 is truly high risk but predicted low risk with `P=0.400`. Changing only `recent_late_payments` from 1 to 2 flips the model to high risk, revealing a likely missed signal. | Counterfactuals explain what would change the model's output, not why the real label was high risk. |\n",
        "| 9. Estimate Trustworthiness | Should a human trust this prediction? | TODO |  |  |\n",
        "| 10. Reverse Engineer Strategy | What strategy has each model learned? | TODO |  |  |\n"
      ]
    },