# Upstream source and synchronization

This repository is a downstream copy of [DWDN by Jiangxin Dong](https://gitlab.mpi-klsb.mpg.de/jdong/dwdn).
Original authors: Jiangxin Dong, Stefan Roth, and Bernt Schiele.

## Attribution

**Deep Wiener Deconvolution: Wiener Meets Deep Learning for Image Deblurring**, Advances in Neural Information Processing Systems 33, 2020.
The original README includes the paper links, BibTeX, requirements, and evaluation instructions and is preserved unchanged at import.

```bibtex
@article{dong2020deep,
  title={Deep Wiener Deconvolution: Wiener Meets Deep Learning for Image Deblurring},
  author={Dong, Jiangxin and Roth, Stefan and Schiele, Bernt},
  journal={Advances in Neural Information Processing Systems},
  volume={33},
  year={2020}
}
```

Imported on 2026-10-27 from upstream `master` at `9018502b88e495c72bfb152e4b1c002d8a0f111d`, retaining the complete Git history, authorship, files, and bundled model. No separate license file was present at import; this copy does not add or change permissions granted by the original authors.

## Branches and automatic updates

- `master` preserves upstream `master` exactly. Do not commit downstream changes there.
- `main` is the default branch. It contains the original project plus this file and the synchronization workflow.
- GitHub Actions checks upstream daily at 03:17 UTC (12:17 Asia/Seoul), and can be run manually from **Actions > Sync GitLab upstream > Run workflow**. Scheduled runs can be delayed by GitHub.
- The workflow fetches upstream `master` and tags, merges `master` into `main`, and pushes both branches and tags atomically without force. Conflicts, rewritten upstream history, or divergent tags fail the run rather than overwrite downstream work. Inspect the failed Actions run and resolve manually.
- This is one-way synchronization from GitLab to GitHub. It does not modify GitLab, mirror issues/releases, delete refs, or automatically import future additional upstream branches.
- Authentication uses the repository's built-in `GITHUB_TOKEN` with `contents: write`; no personal token or GitLab administrator access is required. Actions must remain enabled.

## Local use

```sh
git clone https://github.com/n01r1r/dwdn.git
cd dwdn
git remote add upstream https://gitlab.mpi-klsb.mpg.de/jdong/dwdn.git
git -c http.version=HTTP/1.1 fetch upstream
```

Follow the original [README](README.md) for model dependencies and `python main.py` evaluation. Its PyTorch versions are historical; importing and synchronizing the repository does not establish compatibility with a modern Python/CUDA environment. No model execution or dependency migration was performed as part of the import.
