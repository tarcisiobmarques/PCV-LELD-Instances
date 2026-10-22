# PCV-LELD Benchmark Instances

Benchmark instances for the **Traveling Salesman Problem with Drone Launch Station Location (PCV-LELD)**.

This repository contains **240 benchmark instances** used in computational experiments involving mathematical optimization and the GRASP-RVND, HTLO, and HTLO-RVND metaheuristics.

## Instance Sets

| Source | Number of instances |
|---|---:|
| TSPLIB | 60 |
| CVRPLIB | 180 |
| **Total** | **240** |

The instances are organized into two directories, `TSPLIB/` and `CVRPLIB/`, each containing one subdirectory per instance.

## Instance Structure

Each instance provides the information needed to define the problem, including:

- `deposito.txt`: depot coordinates.
- `estacoes.txt`: candidate drone launch station coordinates.
- `clientes.txt`: customer coordinates and associated information.
- `.png` file: graphical representation of the instance, when available.

## Instance Adaptation

The instances were adapted from the original TSPLIB and CVRPLIB datasets to represent the PCV-LELD.

For TSPLIB instances, candidate launch stations and drone-only customers are selected using a deterministic K-Means-based procedure.

For CVRPLIB instances, the depot, candidate launch stations, and customers are assigned according to the original vertex ordering.

Customers are classified as either drone-only or eligible for service by truck or drone.

In the computational experiments, coordinates are scaled to a 10 × 7 km region, and customer payloads are assigned deterministically using a cyclic sequence from 1.0 to 5.0 kg in increments of 0.25 kg. These transformations are part of the experimental setup.

## Original Data Sources

- [TSPLIB — University of Heidelberg](https://comopt.ifi.uni-heidelberg.de/software/TSPLIB95/)
- [CVRPLIB — Capacitated Vehicle Routing Problem Library](https://galgos.inf.puc-rio.br/cvrplib/)

The original benchmark collections should be acknowledged when using these adapted instances. Rights associated with the source datasets remain with their respective rights holders.

## References

Reinelt, G. (1991). TSPLIB—A Traveling Salesman Problem Library. *ORSA Journal on Computing*, 3(4), 376–384.

Uchoa, E., Pecin, D., Pessoa, A., Poggi, M., Vidal, T., and Subramanian, A. (2017). New benchmark instances for the Capacitated Vehicle Routing Problem. *European Journal of Operational Research*, 257(3), 845–858.

## Research and Reproducibility

These adapted instances support reproducible computational research on the PCV-LELD.

Further details on the mathematical model, instance construction, algorithmic approaches, and computational configuration are provided in the associated research publications.

## Authors

Tarcisio Barroso Marques and José Elias C. Arroyo.
