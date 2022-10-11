# DevSecOps-Pro
Notes for future / Exam

> Pull Zaps docker Image
```bash
docker run --rm owasp/zap2docker-stable:2.10.0 zap-baseline.py --help
```

> Help for Zaps
```bash
docker run --rm owasp/zap2docker-stable:2.10.0 zap-baseline.py --help
```
> Run Zap with basic usage
```bash
docker run --rm owasp/zap2docker-stable:2.10.0 zap-baseline.py -t https://prod-eggkd08x.lab.practical-devsecops.training
```
