# THH-AMQI-002-RSI-ACS

<img width="581" height="852" alt="image" src="https://github.com/user-attachments/assets/05e2d7ed-28cd-4c35-83e8-8f16499e298d" />
<img width="552" height="837" alt="image" src="https://github.com/user-attachments/assets/6480d36f-9a87-4263-97c4-2473322a341d" />
<img width="581" height="852" alt="image" src="https://github.com/user-attachments/assets/96a000dd-8d5c-41d0-86f7-71bcb64b6b59" />
<img width="581" height="362" alt="image" src="https://github.com/user-attachments/assets/179d4e12-fd4a-403a-bece-c9d72ad20382" />

# THH-AMQI-002 — RSI-ACS Computational Core v1.1

<img width="716" height="701" alt="image" src="https://github.com/user-attachments/assets/ad0714fb-307e-4f0c-a2a2-c6ff3b4663f1" />
<img width="832" height="807" alt="image" src="https://github.com/user-attachments/assets/a72968f7-1f9f-4e57-bd04-bcb5a8a829e9" />
<img width="752" height="798" alt="image" src="https://github.com/user-attachments/assets/63f8741b-a3ba-4559-8d5b-7265bc0d2139" />
<img width="791" height="808" alt="image" src="https://github.com/user-attachments/assets/f1eed4d8-c6da-4e96-b855-df3839ab1134" />
<img width="762" height="767" alt="image" src="https://github.com/user-attachments/assets/4cc05f0c-9350-4ee1-9e3a-05f47f09ebec" />
<img width="778" height="696" alt="image" src="https://github.com/user-attachments/assets/2ae05fd5-d1d3-432a-b2d7-7fb381e3cff2" />

# Pseudo:
def rsi_acs(environment, branches, budget):

    while True:
        state = environment.observe()

        failures = analyze_failures(state)

        candidates = discover_root_causes(failures)

        ranked = rank_by_leverage(candidates)

        root = ranked[0]

        hypothesis = generate_hypothesis(root)

        experiment = run_isolated_test(
            environment,
            hypothesis
        )

        evidence = verify_independently(experiment)

        if not evidence.passed:
            reject(hypothesis)
            continue

        improvement = measure_improvement(
            state,
            experiment.result
        )

        if improvement.verified:
            update_knowledge(hypothesis)
            update_branch_performance(branches)

            winner = max(
                branches,
                key=lambda x: x.utility
            )

            allocate_resources(
                branches,
                winner,
                budget
            )

        else:
            rollback(experiment)

        update_evolution_strategy()

---
<img width="751" height="830" alt="image" src="https://github.com/user-attachments/assets/620d46bf-f3d0-4db4-90b2-e1cfe15debed" />
