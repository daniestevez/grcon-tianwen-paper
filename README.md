# GNU Radio flowgraphs for decoding Tianwen-1

This repository is presented as a companion to the article "Deep space reception
of Tianwen-1 by AMSAT-DL using GNU Radio" presented in the [Proceedings of the
GNU Radio Conference](https://pubs.gnuradio.org/index.php/grcon) in 2021. It
contains flowgraphs to decode the telemetry signals of Tianwen-1.

The contents of the repository are the following:

* `tianwen1.grc`. Decoder for the low rate residual carrier telemetry.
* `tianwen1_hsd.grc`. Decoder for the QPSK suppressed carrier telemetry.
* `tianwen1_hsd_shortframes.grc`. Decoder for the QPSK suppressed carrier telemetry
  with short frames.
* `tianwen1_qpsk_lowrate.grc`. Decoder for the QPSK suppressed carrier low rate
  telemetry. This mode is only used very briefly when switching to and from high
  speed data and is not treated in the paper.

The `bochum` folder contains these decoders organized as hierarchical flowgraphs,
which is the approach that was used in the Bochum to interface to the USRP receiver.
The `recording_test.grc` is the top level flowgraph, and the remaining flowgraphs
are hierarchical flowgraphs that contain each of the decoders.

