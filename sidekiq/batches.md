Sidekiq Batches、大好き。

でかい処理を小さい処理に分割して並列処理するのが本来の用途。
だた、batchesだとcallbackの仕組みがあるので、ワークフロー的な処理が実現できる。

https://github.com/sidekiq/sidekiq/wiki/Really-Complex-Workflows-with-Batches

batch.invalidate_allと`status.invalidated?`(callback内) `valid_within_batch?`(ジョブ内)などを使うとworkflowを中断したりはできる
