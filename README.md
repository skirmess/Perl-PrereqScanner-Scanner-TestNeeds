# NAME

Perl::PrereqScanner::Scanner::TestNeeds - scan for modules loaded with Test::Needs

# VERSION

Version 0.001

# SYNOPSIS

    use Perl::PrereqScanner;
    my $scanner = Perl::PrereqScanner->new( { extra_scanners => ['TestNeeds'] } );
    my $prereqs = $scanner->scan_ppi_document($ppi_doc);
    my $prereqs = $scanner->scan_file($file_path);
    my $prereqs = $scanner->scan_string($perl_code);
    my $prereqs = $scanner->scan_module($module_name);

# DESCRIPTION

This is a scanner for [Perl::PrereqScanner](https://metacpan.org/pod/Perl%3A%3APrereqScanner) that finds modules used with
[Test::Needs](https://metacpan.org/pod/Test%3A%3ANeeds).

Note: The scanner currently does not detect modules loaded with the
`test_needs` sub, only modules used with a use statement are detected.

    use Test::Needs 'Some::Module';

# SEE ALSO

[Perl::PrereqScanner](https://metacpan.org/pod/Perl%3A%3APrereqScanner), [Test::Needs](https://metacpan.org/pod/Test%3A%3ANeeds)

# SUPPORT

## Bugs / Feature Requests

Please report any bugs or feature requests through the issue tracker
at [https://github.com/skirmess/Perl-PrereqScanner-Scanner-TestNeeds/issues](https://github.com/skirmess/Perl-PrereqScanner-Scanner-TestNeeds/issues).
You will be notified automatically of any progress on your issue.

## Source Code

This is open source software. The code repository is available for
public review and contribution under the terms of the license.

[https://github.com/skirmess/Perl-PrereqScanner-Scanner-TestNeeds](https://github.com/skirmess/Perl-PrereqScanner-Scanner-TestNeeds)

    git clone https://github.com/skirmess/Perl-PrereqScanner-Scanner-TestNeeds.git

# AUTHOR

Sven Kirmess <sven.kirmess@kzone.ch>

# COPYRIGHT AND LICENSE

This software is Copyright (c) 2021 by Sven Kirmess.

This is free software, licensed under:

    The (two-clause) FreeBSD License
