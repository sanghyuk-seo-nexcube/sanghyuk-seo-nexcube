<table>
  <tr>
    <td valign="top">
      <p>
        <a href="https://github.com/NousResearch/hermes-agent">
          <img src="./assets/hermes-agent-icon.png" alt="Hermes Agent icon" width="72" align="left">
        </a>
        <strong>Hermes Agent ☤ 기여</strong><br>
        <sub>NousResearch/hermes-agent · Codex stream reliability</sub>
      </p>
      <br clear="left">
      <h3>Codex 긴 입력 스트리밍 안정화</h3>
      <p>
        긴 <code>openai-codex</code> 요청에서 backend prefill 지연을
        first-byte 장애로 오판해 불필요하게 reconnect/retry하던 문제를 줄였습니다.
      </p>
      <ul>
        <li><strong>문제:</strong> 큰 컨텍스트 요청은 첫 SSE 이벤트 전에 오래 걸릴 수 있는데, Hermes가 이를 stream 실패로 판단했습니다.</li>
        <li><strong>해결:</strong> 작은 요청 no-event, 큰 요청 prefill 대기, 이벤트 이후 idle을 분리하는 3-case watchdog 정책을 적용했습니다.</li>
        <li><strong>Upstream 반영:</strong> 제 원본 PR <a href="https://github.com/NousResearch/hermes-agent/pull/33383">#33383</a>이 maintainer salvage PR <a href="https://github.com/NousResearch/hermes-agent/pull/33390">#33390</a>로 병합됐습니다.</li>
        <li><strong>근거:</strong> maintainer가 <a href="https://github.com/NousResearch/hermes-agent/pull/33383#issuecomment-4557376403">@sanghyuk-seo-nexcube 멘션과 authorship 보존</a>을 남겼고, 관련 이슈 <a href="https://github.com/NousResearch/hermes-agent/issues/33075">#33075</a>의 large-prefill/no-first-byte 범위를 다뤘습니다.</li>
        <li><strong>범위:</strong> PR 코멘트의 600초 무응답, subagent 동시성, backend silent-reject 리포트는 이 수정과 구분되는 후속 문제로 남아 있습니다.</li>
      </ul>
    </td>
  </tr>
  <tr>
    <td align="center">
      <a href="https://github.com/NousResearch/hermes-agent/pull/33390">
        <img src="https://opengraph.githubassets.com/sanghyuk-hermes-agent-pr33390-card/NousResearch/hermes-agent/pull/33390" alt="PR #33390 thumbnail" width="76%">
      </a>
    </td>
  </tr>
</table>
