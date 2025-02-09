TODOS:
add delete folder ( manual parent deletion )
implement better user management ( add a user table )
code suggested:

<!-- async function deleteFolder(folderId: number) {
  // Delete all files in this folder
  await db.delete(files_table).where(eq(files_table.parent, folderId));

  // Get all subfolders
  const subfolders = await db.select().from(folders_table).where(eq(folders_table.parent, folderId));

  // Recursively delete all subfolders
  for (const subfolder of subfolders) {
    await deleteFolder(subfolder.id);
  }

  // Finally delete the folder itself
  await db.delete(folders_table).where(eq(folders_table.id, folderId));
} -->
