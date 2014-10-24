<style>a{vertical-align:super;font-size:70%;}</style>
[&lt; Home](?README.md)

##Proposal: AOL should start offering free SSL Certificates

*Posted 2014-10-24*

A few months ago, I proposed that Firefox should change its generic
http icon to be a broken lock[1]. This would offer a bit of negative
feedback for websites that do not use https and hopefully encourage
them switching to https. This was obviously a big ask, and it sparked
quite extensive discussions in both the Mozilla[2] and Chromium[3]
security mailing lists. Most people were sympathetic to the goal, but
the bug eventually got closed as Verified Wontfix.

Anyway, two of the recurring arguments against the proposal were:

1. SSL Certificates are expensive.
2. Certificate Authorities are a racket.

I don't necessarily see these as deal breakers to being more
aggressive with https adoption, but I can understand where these
arguments are coming from. StartCom offers a free certificate, but you
have to pay to have it revoked, and a lot people got burned on that
during Heartbleed (including me). I'm not aware of anyone else who
offers a free SSL Certificate, even with the revocation gotcha. So I
can see how the perception is that certs are a cost that isn't worth
it for your personal blog or random side project site. Also, I can
sympathize with the perception that CAs are racket because they all
come across as pretty scammy with their upsells and add-ons that don't
actually add much.

Unfortunately, it seems like any sort of PKI alternative is years if
not decades away, so I began brainstorming short-to-mid-term solutions
to this problem.

I started by looking at the default root certificate repositories that
the major browsers and operating systems use. They are mostly your
regular list of CAs and governments, but there's one name that popped
out as unique: AOL.

America Online has two legacy certificates[4] in the Microsoft[5],
Apple[6], NSS[7], and Android[8] default list of root CAs. I'm
assuming this is from back when AIM as all the rage, but remarkably
AOL has been keeping up the audits[9] for them. Does anyone have any
more info on the history of these certs?

I think might be a great opportunity to address the two problems
above. Could AOL start offering free SSL Certificates?

Pros:

1. Their root certificates are already in everyone's list (backwards
compatibility).
2. Their core business model is not issuing certificates (not seen as a racket).
3. They would get a huge press coverage for being a "savior of HTTPS"
or some such spin (positive spotlight for AOL).
4. There would now be competition in the free SSL cert market (maybe
other CAs would start offering free options, too).

Cons:

1. This would be a cost for AOL. Perhaps other tech companies could
partner with them to subsidize the cost of issuing the certificate?
Perhaps there could be kickstarter to pay for the costs? Perhaps AOL
could spin off a non-profit foundation or donate the certificates to
Mozilla?
2. Unforseen technical problems associated with starting to chain to a
certificate that hasn't been in active use for a long time. I have no
idea what these could be. Thoughts?
3. SSL certs would likely be issued with no warranty (since they are
free). Not a deal breaker in my opinion, because the scope for these
could be for non-commercial use.

Anyway, just tossing out this idea for feedback. There's no sense in
pursuing this further if there's technical reasons making this
impossible. Also, does anyone know anyone who works at AOL? Would
love to talk to someone there.

Daniel Roesler, diafygi@gmail.com

[1]: https://bugzilla.mozilla.org/show_bug.cgi?id=1041087
[2]: https://groups.google.com/forum/#!topic/mozilla.dev.security.policy/iU86qMOwvWs
[3]: https://groups.google.com/a/chromium.org/forum/#!topic/security-dev/rGM2oiKZqZU
[4]: https://pki-info.aol.com/AOL/
[5]: https://social.technet.microsoft.com/wiki/contents/articles/14216.windows-and-windows-phone-8-ssl-root-certificate-program-april-2012-a-d.aspx
[6]: http://support.apple.com/kb/HT5012
[7]: https://www.mozilla.org/en-US/about/governance/policies/security-group/certs/included/
[8]: https://android.googlesource.com/platform/libcore/+/master/luni/src/main/files/cacerts/2fb1850a.0
[9]: https://pki-info.aol.com/AOL/2013_AOLRoot_Audit_Attestation.pdf

