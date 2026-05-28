<table>
  <tr>
    <td valign="top">
      <p>
        <a href="https://github.com/NousResearch/hermes-agent">
          <img src="./assets/hermes-agent-icon.png" alt="Hermes Agent icon" width="72" align="left">
        </a>
        <strong>Hermes Agent ☤</strong><br>
        <sub>NousResearch/hermes-agent · Codex stream compatibility</sub>
      </p>
      <br clear="left">
      <h3>Codex 스트리밍 안정화</h3>
      <p>
        긴 Codex 입력에서 backend prefill 지연을 first-byte 장애로 오판해
        불필요하게 retry하던 흐름을 줄였습니다.
      </p>
      <p>
        큰 컨텍스트는 보존하고, Codex stream 특성에 맞춰 기다릴 구간과
        재연결할 구간을 분리했습니다.
      </p>
      <p>
        <a href="https://github.com/NousResearch/hermes-agent/pull/33390">
          <img src="https://img.shields.io/badge/Merged%20PR-%2333390-238636?style=flat-square&logo=github" alt="Merged PR #33390">
        </a>
        <a href="https://github.com/NousResearch/hermes-agent/commit/283bb810e7211acc38171d3171bb6049ff6d4dba">
          <img src="https://img.shields.io/badge/Commit-283bb810e-0969da?style=flat-square&logo=git" alt="Commit 283bb810e">
        </a>
      </p>
    </td>
  </tr>
  <tr>
    <td align="center">
      <a href="https://github.com/NousResearch/hermes-agent/pull/33390">
        <img src="https://opengraph.githubassets.com/sanghyuk-hermes-agent-pr33390-card/NousResearch/hermes-agent/pull/33390" alt="PR #33390 thumbnail" width="76%">
      </a>
      <sub>
        <a href="https://github.com/NousResearch/hermes-agent/pull/33390">PR #33390</a>
      </sub>
    </td>
  </tr>
</table>
